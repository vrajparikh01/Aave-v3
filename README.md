```shell
# Fill out environment variables inside .env
cp .env.sample .env

# Build exercises
forge build

# Build solutions
FOUNDRY_PROFILE=solution forge build

# Get block number
FORK_BLOCK_NUM=$(cast block-number --rpc-url $FORK_URL)

# Test example
forge test --fork-url $FORK_URL --fork-block-number $FORK_BLOCK_NUM --match-path test/Supply.test.sol -vvv

# Test solution
FOUNDRY_PROFILE=solution forge test --fork-url $FORK_URL --fork-block-number $FORK_BLOCK_NUM --match-path test/Supply.test.sol -vvv

# Try building from scratch if you're having trouble
forge clean
```