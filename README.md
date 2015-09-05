# auction-bot
ottoneu Fantasy Sports auction bot

# WHY

ottoneu Fantasy Sports utilizes auction drafts to distribute players at the
beginning of a season. This is true for baseball and football, and is a
fundamental part of launching a league. However, auction drafts are lengthy
affairs that require 4 to 8 hours, depending on the sport and how long the
league has been active. A client that could take a formatted set of "rules" and
bid on the behalf of a team would make auction drafts faster and more flexible,
which would be a win for ottoneu and a win for ottoneu players.

# HOW

There are certain rules that would be helpful in considering how to bid on the
behalf of an ottoneu team:

- Specific players can be given a budget ($50 for Albert Pujols)
- Specific positions can be given a budget ($200 for OFs)
- Specific positions can be given a player minimum and maximum (7-9 OFs)
- Specific players can be given a priority (Aggressively pursue Andrew Luck)
- Specific positions can be given a priority (RBs are more important than WRs)

More rules should be added here to allow greater control over the behavior of
the auction bot AI. These rules should all be optional, meaning there are both
sensible defaults in place and owners can enact as much or as little control as
they want over those sensible defaults.

# WHAT

Once the bot is enabled on the front-end of the auction draft interface, it
should take over bidding duties for the team's owners until it is disabled. The
technology is ambiguous - should this be run on the front-end? Should this be a
backend script? Should it be its own app that spins up an EC2 instance?

Fundamentally it should behave as any human would utilizing a web browser - it
should request data from the server as often as the web client javascript does,
it should interpret the data utilizing the rules above, and finally it should
make a decision on how to nominate and bid.