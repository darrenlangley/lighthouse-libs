# Lighthouse Libraries

A collection of Rust crates common to the Lighthouse Ethereum 2.0 project.

Related repositories:

- [sigp/lighthouse](https://github.com/sigp/lighthouse) for a project overview
	and integration components.
- [sigp/lighthouse-beacon](https://github.com/sigp/lighthouse-beacon) for the
	beacon node binary.
- [sigp/lighthouse-validator](https://github.com/sigp/lighthouse-validator) for
	the validator client binary.

## Library components:

All library components are Rust crates.

- [`attester`](attester/): a state-machine which fulfils the duties of a Beacon Chain
	attester. Defines traits for communication with the Beacon Node, signing
	services and persistant storage whilst deferring their implementation.
- [`block_producer`](attester/): a state-machine which fulfils the duties of a Beacon Chain
	block producer. Defines traits for communication with the Beacon Node, signing
	services and persistant storage whilst deferring their implementation.
- [`bls`](bls/): wraps an existing BLS cryptography library and provides Eth 2.0
	specific functionality.
- [`boolean-bitfield`](boolean-bitfield/): provides a variable-length `Vec` of `bool`, fulfilling
	the role of the `Bitfield` in the Eth 2.0 spec.
- [`hashing`](hashing/): wraps existing cryptographic hashing libraries and provides Eth
	2.0 specific functionality.
- [`honey-badger-split`](honey-badger-split/): splits a `Vec` into `n` pieces, without fail. Fulfils
	the `split` function of the Eth 2.0 spec.
- [`protos`](protos/): [Google Protocol Buffers](https://developers.google.com/protocol-buffers/)
    used for communications between Lighthouse components.
- [`slot_clock`](slot_clock/): translates the system time into Beacon Chain "slots". Also
	provides a slot clock that's useful during testing.
- [`ssz`](ssz/): an implementation of the SimpleSerialize serialization/deserialization
    protocol used by
	Eth 2.0.
- [`state_processing`](state_processing/): provides the per block/slot/epoch state transition
	functions.
- [`types`](types/): defines all core Eth 2.0 types, such as `BeaconBlock`,
	`BeaconState`, etc.
- [`vec_shuffle`](vec_shuffle/): a pseudo-random Fisher-Yates-Durstenfeld shuffle, which has
	recently been deprecated.

## Contributing

We welcome new contributors and appreciate the efforts of existing
contributors.

If you'd like to help, check for
[good-first-issues](https://github.com/sigp/lighthouse-libs/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)
or reach out in the [gitter](https://gitter.im/sigp/lighthouse) channel.


For detailed onboarding information, see the [lighthouse
documentation](https://github.com/sigp/lighthouse/tree/master/docs).
