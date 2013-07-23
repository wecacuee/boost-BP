# -*- coding: utf-8 -*-

import os

env = Environment(
    CXXFLAGS="-Wall -g -O0",
    LIBS=["stdc++", "pthread"],
    CPPPATH=["#."])
Export("env")
Default(env.SConscript("testings/SConscript"))

prefix = ARGUMENTS.get("prefix", "/usr/local")
prefix_include = os.path.join(prefix, "include")

Alias("install", Install(prefix_include, Dir("cvutil")))
