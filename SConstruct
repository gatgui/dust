import excons
from excons.tools import arnold

env = excons.MakeBaseEnv()

prjs = [
   {  "name": "dust",
      "prefix": "arnold",
      "type": "dynamicmodule",
      "ext": arnold.PluginExt(),
      "srcs": excons.glob("src/dusty.cpp"),
      "install": {excons.OutputBaseDirectory() + "/arnold": excons.glob("src/*.mtd"),
                  excons.OutputBaseDirectory() + "/mtoa/ae": excons.glob("src/*.py")},
      "custom": [arnold.Require]
   }
]

excons.DeclareTargets(env, prjs)
