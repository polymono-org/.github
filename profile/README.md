# A git metaframework for infinitely distributed teams

### Goals

- Don't make devs lives harder
- Must be as ergonomic as Lerna/NX
- Must be nearly as easy diffuculty curve to adopt as a sprawling nighmare of polyrepos 
- Iteratively adopted as compared to the productivity-killing poly->mono transition teams undergo to improve their repository architecture 
- Get all the bells and whistles monorepo.tools advertises
- Don't use git for the metarepo
- No git submodules either
- Metarepo operates in a permissionless setting with no root user
- Runs on the worlds first global singleton computer for unrivalled native atomicity
- Devs do not 'clone' meta repos. They are virtualised instances of a git repo itself
- Store the state root efficiently, produced from an e-merge.
- Pioneer the concept of e-merges "emergent merge operations" - conceptually unlike a normal merge involving molecule<->molecule, this is a meta-level action operating at an organism level compared to molecular level the repository resides at
- Emerge - an Organism emerges from the molecules (commits in child repos) which is the construction of ONLY molecules which the organisms creator permits (meta-perms) it to be created from
- Meta-Build tooling operates at organism level, rather than molecular providing atomicity without requiring a SINGLE change to the underlying child repos. This makes it zero-cost to adopt as it will not distrupt any existing build processes
- Granular permissions controls which allow the metarepo admin to block automated process like CICD if a commit is made by a non-permed comitter
- 

# Methodology

1. Make a commit in a subrepo (child repo)
2. Get the commit hash https://git-scm.com/book/en/v2/Git-Internals-Git-Objects
3. Unwrap the commit SHA and verify the commiter is permissioned 
4. Update the merkle tree with the verified commit hash on the metarepo for permissioned committer
5. Store the root onchain <- Atomic commit (Push)
6. Retrive the root and rebuild a working virtual git tree(s) <- Emerge (Pull)
7. Run automated process like new build deployment from the virtualised tree
8. Rinse and repeat 
