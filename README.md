# kunjung

**kunjung** (from Indonesian *mengunjungi*, to visit) starts from a simple
problem: you hand someone a card, they scan its QR code, and weeks later a
message arrives from a name you do not recognize - where did this contact
come from? A plain contact QR cannot tell you.

This repository holds public research on context-aware contact cards for
Delta Chat, published as one page at
[vanipy.com/kunjung](https://vanipy.com/kunjung/). It is research and a
concept, not a built product: no account, group or purchase is created by
anything here, and every QR code shown is synthetic and joins nothing.

## What the research covers

- **How a Delta Chat invite QR works** - the link shape, why everything
  after `#` never reaches the i.delta.chat server, and why resetting an
  invite invalidates old printed codes. Sources: deltachat/interface
  uri-schemes.md, deltachat/invite, delta.chat/en/help.
- **Four ways to keep the context**, with their real tradeoffs:
  - A. One group per event - exact context, zero per-card work, revocable;
    but group members see each other, and Delta Chat's own help advises
    against sharing groups publicly.
  - B. One private mini-group per person - exact and private; heavy setup,
    one group and one unique print per person.
  - C. A separate profile just for cards - private, low friction; but the
    context is only "came via a card", and stock clients have no unified
    inbox across profiles.
  - D. Plain contact QR plus a printed line - nothing to set up; depends on
    the other person remembering to say where you met.
- **kunjung, the contextual inbox concept** (name and idea only, not
  built): one inbox across your Delta Chat profiles, with each incoming
  conversation tagged by the profile and card context it arrived through.
  The Delta Chat core already runs multiple accounts in one client process,
  so this is a client-UI project, not a protocol change.
- **Small printers that fit this** - thermal label, pocket thermal and
  photo-card bands with Indonesian prices observed on 2026-11-20 (stock and
  promos change; no affiliate links, no purchase made), QR print-sizing
  arithmetic (a ~165-character invite encodes to a 49x49-module QR, so keep
  the print at 28-38 mm on the label), and the open choices: approach,
  media, budget band and volume.

## Handoff demo

`handoff/` is a separate synthetic prototype: a fixed fictional encounter
opens an editable preview in [Jumpa](https://github.com/irvan-putra/jumpa)
0.1.1 or newer on Android. Demo people only, explicit person choice and
save, no automatic sync and no live inbox. The research page and the
unbuilt inbox concept remain separate.

## Notes

- The page's original address <https://vanipy.com/konteks/> remains
  compatible; the repository was renamed from konteks to kunjung without
  replacing history, and old GitHub links redirect.
- Built with public sources linked inline on the page; no personal data is
  published.

---

Built with AI assistance (Instinct and others). Not everything has been reviewed by Irvan. No Fenrir usage in this repo.
