---
layout: other
title: Apktool - Changelog
description: Apktool - Changelog / Roadmap
---

## v2.7.0
2022.11.24
 * Add SDK T (API 33) support. ([Issue 2845](https://github.com/iBotPeaches/Apktool/pull/2845))
 * Add SDK S v2 (API 32) support. ([Issue 2776](https://github.com/iBotPeaches/Apktool/issues/2776))
 * Updated internal aapt/aapt2 to ([91492d8 of frameworks_base](https://github.com/iBotPeaches/platform_frameworks_base/commit/91492d85dcaefe1999ae98d0d2b39258be2252a9))
 * Add support for newest `ResourcesTypes.h` specs (policy, overlay and staged alias). ([Issue 2809](https://github.com/iBotPeaches/Apktool/issues/2809), [Issue 2714](https://github.com/iBotPeaches/Apktool/issues/2714))
 * Add updated internal aapt2/aapt2 binaries. ([Issue 2787](https://github.com/iBotPeaches/Apktool/pull/2787))
 * Add ability to generate generic network security config (`-n` / `--net-sec-conf`). ([Issue 1622](https://github.com/iBotPeaches/Apktool/issues/1622))
 * Add helpful message during built apk message to identify location of apk. ([Issue 2843](https://github.com/iBotPeaches/Apktool/issues/2843))
 * Add bleeding edge smali package via jitpack. ([Issue 2918](https://github.com/iBotPeaches/Apktool/issues/2918), [Issue 2662](https://github.com/iBotPeaches/Apktool/issues/2662))
 * Add build support for JDK 17. ([Issue 2952](https://github.com/iBotPeaches/Apktool/pull/2952))
 * Fix resource unclosed during unknown file handling. ([Issue 2473](https://github.com/iBotPeaches/Apktool/issues/2473)) / (Thanks 
auermich93)
 * Fix style strings regression between aapt1/aapt2 builds. ([Issue 2815](https://github.com/iBotPeaches/Apktool/issues/2815)) / (Thanks IgorEisberg)
 * Fix support for `uses-native-library` in Manifest. ([Issue 2778](https://github.com/iBotPeaches/Apktool/issues/2778))
 * Fix support for `usesPermissionFlags` in Manifest. ([Issue 2789](https://github.com/iBotPeaches/Apktool/issues/2789))
 * Fix windows helper script to allow spaces in path name. ([Issue 2855](https://github.com/iBotPeaches/Apktool/issues/2855))
 * Fix decoding application if using multiple style res types. ([Issue 1719](https://github.com/iBotPeaches/Apktool/issues/1719)) / (Thanks tvildo)
 * Fix handling with malformed namespaces. ([Issue 2615](https://github.com/iBotPeaches/Apktool/issues/2615)) / (Thanks ljysdfz & MyAnoneNeko)
 * Fix handling of sparse flags during resource parsing. ([Issue 2887](https://github.com/iBotPeaches/Apktool/pull/2887)) / (Thanks iamr0s)
 * Fix crash when parsing a manifest numeric that resolves as null. ([Issue 2878](https://github.com/iBotPeaches/Apktool/issues/2878))
 * Fix crash when parsing HTML string with empty tag leading to invalid entry. ([Issue 2900](https://github.com/iBotPeaches/Apktool/issues/2900)) / (Thanks MaSven)
 * Fix crash when wrongly decoding overlay policies. ([Issue 2805](https://github.com/iBotPeaches/Apktool/issues/2805)) / (Thanks gramound)
 * Fix regression when decoding overlay policies. ([Issue 2945](https://github.com/iBotPeaches/Apktool/issues/2945))
 * Fix respecting of `$XDG_DATA_HOME` on Linux for framework files location. ([Issue 2924](https://github.com/iBotPeaches/Apktool/pull/2924)) / (Thanks Miepee)
 * Fix storing of obfuscated resource files for properly applying proper compression on build. ([Issue 2925](https://github.com/iBotPeaches/Apktool/pull/2925)) / (Thanks Kirlif)
 * Fix issue parsing an obfuscated resource with a improperly referenced parent resource. ([Issue 2908](https://github.com/iBotPeaches/Apktool/issues/2908))
 * Fix `--only-main-classes` winning over `--no-src`. ([Issue 2927](https://github.com/iBotPeaches/Apktool/pull/2927)) / (Thanks Surendrajat)
 * Fix disassembly of files mixed between `r`, `R` and `res` folders. ([Issue 2933](https://github.com/iBotPeaches/Apktool/issues/2933))
 * Fix handling of `(name removed)` resources. ([Issue 2940](https://github.com/iBotPeaches/Apktool/pull/2940)) / (Thanks Danealau)
 * Fix disassembly of raw resources for AndResGuard. ([Issue 2943](https://github.com/iBotPeaches/Apktool/pull/2944))
 * Fix attribute referencing to self package while using AndResGuard. ([Issue 2911](https://github.com/iBotPeaches/Apktool/issues/2911))
 * Revert automatic workaround for using private resources. ([PR 2785](https://github.com/iBotPeaches/Apktool/pull/2785), [Issue 2771](https://github.com/iBotPeaches/Apktool/issues/2771))
 * Upgrade CI Workflow to leverage latest actions. (Thanks Goooler)
 * Upgrade `org.apache.commons:commons-text` to `1.10.0` (from `1.9`)
 * Upgrade `org.yaml:snakeyaml` to `1.32` (from `1.29`)

## v2.6.1
2022.02.26
 * Add `apktool-cli` to Maven publishing. ([Issue 2686](https://github.com/iBotPeaches/Apktool/issues/2686))
 * Add support for signature scheme v4 ([Issue 2687](https://github.com/iBotPeaches/Apktool/issues/2687))
 * Add `commons-lang` project to remove deprecated methods from `commons-io`. ([Issue 2713](https://github.com/iBotPeaches/Apktool/pull/2713/files)) (Thanks alsutton)
 * Upgrade to `commons-cli 1.5.0` (Thanks Goooler)
 * Upgrade to `guava 31.0.1` (Thanks Goooler)
 * Upgrade to `jengelman.shadow 7.1.0` (Thanks Goooler)
 * Fix `licenseFormat[Test/Main]` to properly inject variables into license preamble.
 * Fix temp files being written into `/tmp` and not automatically removed. ([Issue 2739](https://github.com/iBotPeaches/Apktool/issues/2739))
 * Support automatic workaround for using private resources. ([Issue 2637](https://github.com/iBotPeaches/Apktool/issues/2637)) (Thanks MrIkso)

## v2.6.0
2021.09.02
 
 * **Android 12 Support** ([Issue 2580](https://github.com/iBotPeaches/Apktool/issues/2580))
 * Published to Maven Central ([Issue 2529](https://github.com/iBotPeaches/Apktool/issues/2529))
 * Upgrade internal aapt/aapt2 to ([7691c of frameworks_base](https://github.com/iBotPeaches/platform_frameworks_base/commit/63f688ebacc6a92ddf298ef6a88edc996017691c))
 * Upgrade to baksmali/smali 2.5.2
 * Upgrade to `gradle 7.2` (Thanks Goooler)
 * Upgrade to `snakeyaml 1.29` (Thanks Goooler)
 * Upgrade to `guava 30.1.1-jre` (Thanks Goooler)
 * Upgrade to `junit 4.13.2` (Thanks Goooler)
 * Upgrade to `commons-lang 3.12.0` (Thanks Goooler)
 * Upgrade to `commons-io 2.11.0` (Thanks Goooler)
 * Upgrade to `proguard 7.1.1` (Thanks Goooler)
 * Upgrade to `license.hierynomus 0.16.1` (Thanks Goooler)
 * Upgrade to `jengelman.shadow 7.0.0` (Thanks Goooler)
 * Upgrade to `actions/setup-java@v2` (Thanks Goooler)
 * Added `.gitattributes` (Thanks Goooler)
 * Added support for SDK in Development (Tiramisu, API 32?)
 * Added automatic execution of aapt/aapt2 binaries during CI process to find broken builds.
 * Added automatic `ldd/otool -L` execution during CI process to identify non-static "fat" aapt/aapt2 builds.
 * Added test execution on Java 15/16 (Now 8-16) during CI process.
 * Upgrade aapt2 with patches for `attr-private` and remove reserved pkgIds. (Thanks MrIkso)
 * Upgrade aapt1 with patches for a static binary on Mac arch.
 * Add lazy init for ResTable for optimizations. ([Issue 2604](https://github.com/iBotPeaches/Apktool/pull/2604)) / (Thanks IgorEisberg)
 * Add automatic disassemble/assemble JAR files without specifying api level. ([Issue 2605](https://github.com/iBotPeaches/Apktool/pull/2605)) / (Thanks IgorEisberg)
 * Changed zipslip exceptions to skip file instead of exit on failure. ([Issue 2201](https://github.com/iBotPeaches/Apktool/issues/2201))
 * Changed dummy resource names to `APKTOOL_DUPLICATE_{Type}_{RESID}` to prevent starting with numeric ([Issue 2229](https://github.com/iBotPeaches/Apktool/issues/2229))
 * Changed all Apache License links to `https`. ([Issue 2635](https://github.com/iBotPeaches/Apktool/pull/2635)) / (Thanks Goooler)
 * Changed `getHTML()` processor to leverage BundleTool for handling complex string values. ([Issue 2632](https://github.com/iBotPeaches/Apktool/issues/2632)) / (Thanks itaybia)
 * Fix decoding issue requiring specific order of chunks (library/table). ([Issue 2099](https://github.com/iBotPeaches/Apktool/issues/2099)) / (Thanks LoyieKing)
 * Fix decoding issues with code points over > 0x10000. ([Issue 2299](https://github.com/iBotPeaches/Apktool/issues/2299)) / (Thanks Comnir)
 * Fix decoding issues with surrogate pair emojis. ([Issue 2546](https://github.com/iBotPeaches/Apktool/issues/2546)) / (Thanks Comnir)
 * Fix NPE when decoding to a custom non-empty root directory. ([Issue 2455](https://github.com/iBotPeaches/Apktool/issues/2455))
 * Fix Android 11 dex NPE due to hidden api restriction flags. ([Issue 2499](https://github.com/iBotPeaches/Apktool/issues/2499)) / (Thanks JesusFreke)
 * Fix dummy resources being built as type resources vs item resources. ([Issue 2603](https://github.com/iBotPeaches/Apktool/issues/2603))
 * Fix numeric string meta-data losing context of data type. ([Issue 2611](https://github.com/iBotPeaches/Apktool/issues/2611)) / (Thanks codylund)
 * Reduce code smell failures. ([Issue 2554](https://github.com/iBotPeaches/Apktool/pull/2554)) / (Thanks matteobaccan)
 * Reduce code smells & correct improper opcode use for baksmali. ([Issue 2604](https://github.com/iBotPeaches/Apktool/pull/2604)) / (Thanks IgorEisberg)
 * Reduce code smells for unused logic, unneeded casting and newer Java language features. ([Issue 2636](https://github.com/iBotPeaches/Apktool/pull/2636) / (Thanks Goooler)
 * Remove unused `targetSdkVersion` for source disassemble as value was not populated yet. ([Issue 2604](https://github.com/iBotPeaches/Apktool/pull/2604)) / (Thanks IgorEisberg)
 * Remove duplicate workflows for 1 unified GitHub Action workflow. ([Issue 2633](https://github.com/iBotPeaches/Apktool/pull/2633)) / (Thanks Goooler)

## v2.5.0
2020.12.02

 * **Android 11 Support** ([Issue 2399](https://github.com/iBotPeaches/Apktool/issues/2399), [Issue 2397](https://github.com/iBotPeaches/Apktool/issues/2397), [Issue 2369](https://github.com/iBotPeaches/Apktool/issues/2369), [Issue 2167](https://github.com/iBotPeaches/Apktool/issues/2167))
 * Updated baksmali/smali to version 2.4.0 ([Issue 2006](https://github.com/iBotPeaches/Apktool/issues/2006), [Issue 1718](https://github.com/iBotPeaches/Apktool/issues/1718))
 * Upgrade to `gradle 6.4.1`
 * Replaced TravisCI with GitHub Actions
 * Deprecate 32bit ([Issue 2110](https://github.com/iBotPeaches/Apktool/issues/2210), [Issue 2053](https://github.com/iBotPeaches/Apktool/issues/2053))
 * Added support for SDK Codename "S" (Android 12?)
 * Added support for `JAVA_HOME` environmental on Windows if defined. (Thanks vldmrrr)
 * Update license headers to reflect start copyright date & remove javadoc style. (Thanks friederbluemle)
 * Fixed issue with binary name clash in multi-threaded environments. ([Issue 2251](https://github.com/iBotPeaches/Apktool/issues/2251)) Thanks chris-sharl
 * Fixed issue with `resources.arsc` file being compressed in framework files. ([Issue 2323](https://github.com/iBotPeaches/Apktool/issues/2323))
 * Fixed issue with empty files being compressed breaking applications. ([Issue 2333](https://github.com/iBotPeaches/Apktool/issues/2333)) / (Thanks peret)
 * Fixed handling with debug mode while using aapt2. ([Issue 2328](https://github.com/iBotPeaches/Apktool/issues/2328), [Issue 2364](https://github.com/iBotPeaches/Apktool/issues/2364)) / Thanks Comnir)
 * Fixed issue with handling of XML files using `$` in resource name. ([Issue 2386](https://github.com/iBotPeaches/Apktool/issues/2386), [Issue 2217](https://github.com/iBotPeaches/Apktool/issues/2271), [Issue 2119](https://github.com/iBotPeaches/Apktool/issues/2119))
 * Fixed issue with NPE disassembling manifest with attributes with no resourceId. ([Issue 2300](https://github.com/iBotPeaches/Apktool/issues/2300))
 * Fixed issue with aapt2 and strict dummy properties, changing bool(false) to ref(null). ([Issue 2438](https://github.com/iBotPeaches/Apktool/issues/2438), [Issue 1903](https://github.com/iBotPeaches/Apktool/issues/1903))
 * Fixed issue with non-standard namespaces in obfuscated application. ([Issue 2317](https://github.com/iBotPeaches/Apktool/issues/2317), [Issue 2188](https://github.com/iBotPeaches/Apktool/issues/2188), [Issue 1859](https://github.com/iBotPeaches/Apktool/issues/1859))
 * Fixed NPE when trying to find a referent of a missing resource. ([Issue 1945](https://github.com/iBotPeaches/Apktool/issues/1945), [Issue 2146](https://github.com/iBotPeaches/Apktool/issues/2146))
 * Properly return non-zero error if invalid parameters. (Thanks Giszmo)
 * Added helpful error message when framework directory cannot be written. ([Issue 2343](https://github.com/iBotPeaches/Apktool/issues/2343))
 * Added testcases for `classes#.dex` disassembling on aapt1/aapt2. ([Issue 2411](https://github.com/iBotPeaches/Apktool/issues/2411))
 * Added `apktool list-frameworks`. ([Issue 1913](https://github.com/iBotPeaches/Apktool/issues/1913))
 * Support for new `compileSdkVersion` property for `SdkInfo`. ([Issue 2368](https://github.com/iBotPeaches/Apktool/issues/2368))

## v2.4.1
2019.11.19

 * Updated baksmali/smali to version 2.3.4
 * Upgrade to `gradle 5.6.2`
 * Added support for Android Q (10) Final. ([Issue 2131](https://github.com/iBotPeaches/Apktool/issues/2131))
 * Fixed build issue with JDK9+ because of jmod change. ([Issue 2086](https://github.com/iBotPeaches/Apktool/issues/2086))
 * Fixed security issue with unpacking assets to unintended locations via directory traversal. ([Issue 2058](https://github.com/iBotPeaches/Apktool/pull/2058))
 * Fixed issue with api-level command not showing in advanced documentation. ([Issue 2027](https://github.com/iBotPeaches/Apktool/issues/2027))
 * Fixed issue with directory creation warning when framework directory not made. ([Issue 2048](https://github.com/iBotPeaches/Apktool/issues/2048))
 * Fixed issue with missing mapping for `Q` shorthand property. ([Issue 2045](https://github.com/iBotPeaches/Apktool/issues/2045))
 * Fixed issue with raw `qmg` files not decoding correctly. ([Issue 2046](https://github.com/iBotPeaches/Apktool/issues/2064))
 * Fixed issue with copying assets where output directory doesn't match initial structure. ([Issue 2046](https://github.com/iBotPeaches/Apktool/issues/2064))
 * Fixed issue with NPE with empty attribute content during deserialization. ([Issue 2063](https://github.com/iBotPeaches/Apktool/issues/2063))
 * Fixed removal of META-INF/services. ([Issue 2084](https://github.com/iBotPeaches/Apktool/issues/2084), [Issue 2018](https://github.com/iBotPeaches/Apktool/issues/2018)) Thanks adibfara
 * Fixed support for "attr" bag type. ([Issue 2117](https://github.com/iBotPeaches/Apktool/issues/2117)) Thanks visigoth
 * Fixed wiping license headers of AOSP/Android4Me files. ([Issue 2093](https://github.com/iBotPeaches/Apktool/issues/2093))
 * Added enhanced wrapper file for Windows. ([Issue 2120](https://github.com/iBotPeaches/Apktool/pull/2120)) Thanks Varstahl
 * Added advance command for skipping disassemble of non-root dex packages. ([Issue 2051](https://github.com/iBotPeaches/Apktool/pull/2051))
 * Fixed issue with MIUI package names being renamed. ([Issue 2028](https://github.com/iBotPeaches/Apktool/pull/2028)) Thanks IgorEisberg
 * Work-around with issue with large 9patch path spamming in uncompressed file list. ([Issue 1272](https://github.com/iBotPeaches/Apktool/issues/1272)) Thanks IgorEisberg
 * Fixed issue with NPE on annotations ([Issue 2071](https://github.com/iBotPeaches/Apktool/issues/2071))
 * Fixed issue with garbled attributes ([Issue 1576](https://github.com/iBotPeaches/Apktool/issues/1576)) Thanks brianairb
 * Fixed regression with `--only-main-classes` ([Issue 2226](https://github.com/iBotPeaches/Apktool/pull/2226)) Thanks realityJie
 * Fixed 32bit binary issue with Window aapt/aapt2 builds. ([Issue 2141](https://github.com/iBotPeaches/Apktool/issues/2141)) Thanks Furniel
 * Fixed issue with JVM not knowing bitness on Windows in some situations. ([Issue 2105](https://github.com/iBotPeaches/Apktool/issues/2105))
 * Fixed issue with long path commands due to recording compression. ([Issue 1272](https://github.com/iBotPeaches/Apktool/issues/1272)) Thanks peret

## v2.4.0
2019.03.02

 * Java 8 (1.8) is now required.
 * Updated baksmali/smali to version 2.2.6 ([Issue 1893](https://github.com/iBotPeaches/Apktool/issues/1893))
 * Fixed issue with new restriction with non-empty `ids.xml` values. ([Issue 1918](https://github.com/iBotPeaches/Apktool/issues/1918)) / Thanks gino247
 * Fixed issue with `PlatformBuildVersion` properties changing to unexpected values. ([Issue 1909](https://github.com/iBotPeaches/Apktool/issues/1909)) / Thanks gino247
 * Fixed issue with pending v5 Gradle upgrade, by upgrading to gradle v4.10.2. ([Issue 1943](https://github.com/iBotPeaches/Apktool/pull/1943)) / Thanks friederbluemle
 * Added `no-crunch` support (optional) via new parameter of `nc | --no-crunch`. ([Issue 1849](https://github.com/iBotPeaches/Apktool/pull/1849)) / Thanks Novex
 * Fixed issue with `xsd` files decoding/building improperly between aapt1/aapt2. ([Issue 1952](https://github.com/iBotPeaches/Apktool/issues/1952))
 * Fixed issue with malformed chunk header when decoding "special" apks. ([Issue 1976](https://github.com/iBotPeaches/Apktool/issues/1976)) / Thanks sebras
 * Fixed issue with Apktool stealing focus on Mac environments. ([Issue 1996](https://github.com/iBotPeaches/Apktool/issues/1996))
 * Fixed issue with `array` resources having wrong types. ([Issue 1994](https://github.com/iBotPeaches/Apktool/issues/1994)), ([Issue 1922](https://github.com/iBotPeaches/Apktool/issues/1922)) / Thanks vbarthel-fr
 * Fixed issue with 9patch images missing vertical or horizontal divs, by automatically creating them. ([Issue 1522](https://github.com/iBotPeaches/Apktool/issues/1522)) / Thanks IgorEisberg
 * Fixed issue with resolving references to non-standard framework files. / Thanks IgorEisberg
 * Fixed issue with resolving SDK version codes were not explicit values. / Thanks IgorEisberg
 * Added 32bit binaries for unix & windows for `aapt` and `aapt2`.
 * Added automated tests on Windows. ([Issue 1975](https://github.com/iBotPeaches/Apktool/issues/1975))
 * Added ability for `api-level` to be passed to baksmali & smali. / Thanks IgorEisberg

## v2.3.4
2018.09.05

 * **Android Pie Final Support** ([Issue 1864](https://github.com/iBotPeaches/Apktool/issues/1864))
 * Fixed issue with rebuilding applications with `$` or `_` characters (aapt2 only). ([Issue 1776](https://github.com/iBotPeaches/Apktool/issues/1776))
 * Fixed process executor to wait for response (15 seconds) in the case of identifying aapt version. ([Issue 1809](https://github.com/iBotPeaches/Apktool/issues/1809)) / Thanks sunshouxiang
 * Fixed issue with 0 size file being marked as doNotCompress. ([Issue 1843](https://github.com/iBotPeaches/Apktool/issues/1843)) /  Thanks alexeikh
 * Updated aapt2 to latest version to handle various edge cases. ([Issue 1817](https://github.com/iBotPeaches/Apktool/issues/1817))
 * Align the `frameworks/base` project for both `aapt1/aapt2` builds. ([Issue 1889](https://github.com/iBotPeaches/Apktool/issues/1889))
 * Update to Gradle 4.10 and fix warnings with upgrade. ([Issue 1884](https://github.com/iBotPeaches/Apktool/issues/1884))

## v2.3.3
2018.04.26

 * Fixed regression with compressing default AOSP filetypes like mp3. ([Issue 1769](https://github.com/iBotPeaches/Apktool/issues/1769))
 * Fixed detection of aapt2 builds older than certain SDK versions. ([Issue 1774](https://github.com/iBotPeaches/Apktool/issues/1774))

## v2.3.2
2018.04.07

 * **Android P Preview Support** ([Issue 1742](https://github.com/iBotPeaches/Apktool/issues/1742))
 * Initial support for rebuilding with aapt2 binary ([Issue 1689](https://github.com/iBotPeaches/Apktool/issues/1689))
 * Fixed issue with application with empty resources.arsc file ([Issue 1730](https://github.com/iBotPeaches/Apktool/issues/1730))
 * Fixed issue with root depth kotlin folder ([Issue 1703](https://github.com/iBotPeaches/Apktool/issues/1703))
 * Fixed building Apktool on Windows. ([Issue 1741](https://github.com/iBotPeaches/Apktool/issues/1741))
 * Added warning if application is non-zero typeIdOffset is discovered.
 * Update to baksmali v2.2.2
 * Support for treating additional photo extensions as raw (m4a)
 * Prevent temporary BRUT files from clogging temp directories.

## v2.3.1
2017.12.26

 * **Android Oreo Support (8.1)** ([Issue 1667](https://github.com/iBotPeaches/Apktool/issues/1667))
 * Feature: Advanced `--force-manifest` for decoding manifest without resources. ([Issue 1680](https://github.com/iBotPeaches/Apktool/pull/1680)) / Thanks rubenanagua
 * Fixed issue with shorthand SDK versions. ([Issue 1630](https://github.com/iBotPeaches/Apktool/issues/1630))
 * Fixed issue with encoding raw font files. ([Issue 1662](https://github.com/iBotPeaches/Apktool/issues/1662)) / Thanks minsko
 * Fixed issue with rebuilding an apk that skipped resource decoding. ([Issue 1634](https://github.com/iBotPeaches/Apktool/issues/1634))
 * Fixed issue with large string decoding length incorrectly. ([Issue 1587](https://github.com/iBotPeaches/Apktool/issues/1587))
 * Fixed issue to allow repeated entry offsets to occur. ([Issue 1683](https://github.com/iBotPeaches/Apktool/pull/1683)) / Thanks Bricnic
 * Fixed issue where non-system attributes were decoded as system in minified resource applications. ([Issue 1157](https://github.com/iBotPeaches/Apktool/issues/1157))

## v2.3.0
2017.09.21
 
 * **Android Oreo Support** ([Issue 1594](https://github.com/iBotPeaches/Apktool/issues/1594))
 * Run CI tests on OSX as well as unix. ([Issue 1571](https://github.com/iBotPeaches/Apktool/issues/1571))
 * Prevent apktool doing permission checks on unneeded directories. ([Issue 1586](https://github.com/iBotPeaches/Apktool/issues/1586))
 * Windows Unicode support for helper scripts. ([Issue 1595](https://github.com/iBotPeaches/Apktool/issues/1595))
 * Dropped support for all 32 bit binaries, except Windows ([Issue 1598](https://github.com/iBotPeaches/Apktool/issues/1598))
 * Fixed `ClassCastExceptions` when producing files. ([Issue 1444](https://github.com/iBotPeaches/Apktool/issues/1444)) / Thanks xpirt
 * Fixed unclosed streams when using `SmaliMod`. Thanks footpatch
 * Cleanup deprecations in Apache Commons CLI. Thanks xpirt
 * Fixed issue with apks that have 4 non-positional/positional nodes. ([Issue 1611](https://github.com/iBotPeaches/Apktool/issues/1611))
 * Added support for invalid `targetSdkValues` which are greater than `max` or less than `min`. ([Issue 1615](https://github.com/iBotPeaches/Apktool/pull/1615)) / Thanks Jan Vidar Krey
 * Added ability to skip assets decode (`--no-assets`) ([Issue 1605](https://github.com/iBotPeaches/Apktool/issues/1605))
 * Prevented directories being written outside of scope of decode directory. ([Issue 1589](https://github.com/iBotPeaches/Apktool/issues/1589))

## v2.2.4
2017.07.29

 * **Android O Final Dev Preview Support** ([Issue 1520](https://github.com/iBotPeaches/Apktool/issues/1520))
 * Update SnakeYAML to 1.1.8 (Android). ([Issue 591](https://github.com/iBotPeaches/Apktool/issues/591))
 * Upgrade to `gradle 4.0`
 * Fixed issue with APKs taking longer than usual to parse resources. ([Issue 1489](https://github.com/iBotPeaches/Apktool/issues/1489)) / Thanks MarcMil
 * Fixed issue with internal binaries not accessible in a Spring boot environment. ([Issue 1543](https://github.com/iBotPeaches/Apktool/issues/1543)) / Thanks bingqiao
 * Add preliminary support for rebuilding applications built in `aapt2` ([Issue 1520](https://github.com/iBotPeaches/Apktool/issues/1520))
 * Add support for resource filenames to contain `$` symbols. ([Issue 1532](https://github.com/iBotPeaches/Apktool/issues/1532))
 * Fixed issue with apktool not closing file resources, creating locks. ([Issue 1561](https://github.com/iBotPeaches/Apktool/pull/1561)) / Thanks MarcMil
 * Fixed issue with APKs that have `INVALID TYPE CONFIG` resources. ([Issue 1534](https://github.com/iBotPeaches/Apktool/issues/1534))
 * Fixed decoding issue with APKs with intentionally invalid characters. ([Issue 1564](https://github.com/iBotPeaches/Apktool/issues/1564))
 * Only exit with a 0 status code during `version` commands.
 * Enforce proper Apache licenses on all Java files.
 * Prevent malicious directory traversal with unknown files.
 * Prevent XML-XXE processing to prevent unintended leaking of information in a malicious setting.

## v2.2.3
2017.06.13

 * **Android O Preview Support** ([Issue 1453](https://github.com/iBotPeaches/Apktool/issues/1453))
 * Updated to [smali 2.2.1](https://github.com/JesusFreke/smali/wiki/SmaliBaksmali2.2)
 * Updated internal aapt binaries to `android-7.1.2_r11`
 * Removed deprecated fatJar plugin in favor of ShadowJar
    * This turns `fatJar` to `shadowJar` on build instructions.
 * Updated gradle to `v3.5`. Thanks friederbluemle
 * Fix for reading length of UTF16 encoded strings. Thanks atn1969
 * Fixed issue changing default parameters on baksmali. ([Issue 1481](https://github.com/iBotPeaches/Apktool/issues/1481))
 * Fixed issue with apktool locking access to input files. ([Issue 1160](https://github.com/iBotPeaches/Apktool/issues/1160)) Thanks MarcMil
 * Add support for animated vector drawables. ([Issue 1456](https://github.com/iBotPeaches/Apktool/issues/1456))
 * Fixes decoding brightness. ([Issue 1508](https://github.com/iBotPeaches/Apktool/issues/1508)) Thanks phhusson
 * Prevent unknown file decode outside of archive. ([Issue 1498](https://github.com/iBotPeaches/Apktool/issues/1498)) / Thanks mkilling
 * Fixes improper decoding of optical bounds in images. ([Issue 1511](https://github.com/iBotPeaches/Apktool/issues/1508)) Thanks phhusson

## v2.2.2
2017.01.23

 * Added Android 7.1 Resources ([Issue 1349](https://github.com/iBotPeaches/Apktool/issues/1349))
 * Update `aapt` to `android-7.1.1_r4`.
 * Upgrade to `gradle 3.3`
 * Fixed NPE with styles that had a parent that didn't exist. ([Issue 1370](https://github.com/iBotPeaches/Apktool/issues/1370))
 * Fixed issue with `TYPE_DYNAMIC_ATTRIBUTE` treating improperly which affected Nougat based applications. ([Issue 1382](https://github.com/iBotPeaches/Apktool/issues/1382)) / Thanks xpirt
 * Fixed issue with APKs that have invalid characters. ([Issue 885](https://github.com/iBotPeaches/Apktool/issues/885)), ([Issue 1389](https://github.com/iBotPeaches/Apktool/issues/1389))
 * Fixed issue with versioning vector images during build. ([Issue 1384](https://github.com/iBotPeaches/Apktool/issues/1384))
 * Fixed issue with APKs that have invalid characters in filename. ([Issue 1369](https://github.com/iBotPeaches/Apktool/issues/1369))
 * Fixed build issue where space was in build path. ([Issue 1394](https://github.com/iBotPeaches/Apktool/issues/1394))
 * Fixed issue with APKs that have 3 non positional attributes. ([Issue 1360](https://github.com/iBotPeaches/Apktool/issues/1360))
 * Fixed issue with APKs that require non-standard `pkgId`. ([Issue 1119](https://github.com/iBotPeaches/Apktool/issues/1119)), ([Issue 989](https://github.com/iBotPeaches/Apktool/issues/989)), ([Issue 1278](https://github.com/iBotPeaches/Apktool/issues/1278)), ([Issue 1377](https://github.com/iBotPeaches/Apktool/issues/1377)), ([Issue 1091](https://github.com/iBotPeaches/Apktool/issues/1091)) / Thanks peter23
 * Fixed issue with APKs that used reserved words `do` and `if`. ([Issue 1404](https://github.com/iBotPeaches/Apktool/issues/1404))

## v2.2.1
2016.10.18

 * **Android Nougat Support.** ([Issue 1223](https://github.com/iBotPeaches/Apktool/issues/1223))
 * Fixed issue with missing attributes (using Android N Final Preview Sdk). ([Issue 1243](https://github.com/iBotPeaches/Apktool/issues/1243))
 * Fixed issue with new value type 8 - `TYPE_DYNAMIC_ATTRIBUTE`. ([Issue 1317](https://github.com/iBotPeaches/Apktool/issues/1317))
 * Gracefully handle APKs with additional data after `TYPE` chunks. ([Issue 1324](https://github.com/iBotPeaches/Apktool/pull/1324)) / Thanks jamestut
 * Pass `minSdkVersion` to smali to correctly trigger edge cases where proper API needs to set. ([Issue 1313](https://github.com/iBotPeaches/Apktool/pull/1313)) / Thanks benjamin-promon
 * Added `empty-framework-dir` command to cleanup framework directory to ease upgrades. ([Issue 901](https://github.com/iBotPeaches/Apktool/issues/901))
 * Handle applications that trick apktool with unknown header type. ([Issue 1332](https://github.com/iBotPeaches/Apktool/issues/1332)) / Thanks xpirt

## v2.2.0
2016.08.07

 * [Migration Instructions from 2.1.1 to 2.2.0]({{ site.github.url }}/documentation/#v2-1-1-v2-2-0)
 * Updated smali/baksmali to `v2.1.3`
   * Fixed upstream issue where debug comment indexes can cause out of bounds exception. ([Issue 1269](https://github.com/iBotPeaches/Apktool/issues/1269))
 * Default framework changed on Windows & Unix to prevent visible top level home directories. ([Issue 1277](https://github.com/iBotPeaches/Apktool/issues/1277))
 * Fixed issue where extensions would be different cases. ([Issue 1258](https://github.com/iBotPeaches/Apktool/issues/1258))
 * Fixed issue with APKs that had no `versionCode` / `versionName` properties. ([Issue 1264](https://github.com/iBotPeaches/Apktool/issues/1264))
 * Fixed issue with improper decoding of `@empty` value. ([Issue 1270](https://github.com/iBotPeaches/Apktool/issues/1270)) / Thanks phhusson
 * Fixed issue with improper compression with files with multiple extensions. ([Issue 1244](https://github.com/iBotPeaches/Apktool/issues/1244))
 * Fixed issue with overflow for applications that have absurdly large TypeSpec indexes. ([Issue 1185](https://github.com/iBotPeaches/Apktool/issues/1185))
 * Fixed issue with hex values being truncated in `AndroidManifest.xml`. ([Issue 972](https://github.com/iBotPeaches/Apktool/issues/972))
 * Replaced public domain LittleEndianReader for Google's Guava LittleEndianDataInputStream (Apache2). ([Issue 1166](https://github.com/iBotPeaches/Apktool/issues/1166)) / Thanks amorris
 * Fixed issue with APKs that have duplicate value names by creating dummy names. ([Issue 894](https://github.com/iBotPeaches/Apktool/issues/894))
 * Adjust mac and unix scripts to force UTF8 file encoding.
 * Fixed public resource reference error when using references in `android:scheme` in `AndroidManifest.xml`. ([Issue 1097](https://github.com/iBotPeaches/Apktool/issues/1097))
 * Fixed issue with APKs where parent reference in `styles.xml` is not found. ([Issue 745](https://github.com/iBotPeaches/Apktool/issues/745))

## v2.1.1
2016.05.07

 * Fixed issue where APK would identify as wrong `packageId` ([Issue 1220](https://github.com/iBotPeaches/Apktool/issues/1220))
 * Include the `AndroidManifest.xml` file from the framework being installed to satisfy default aapt. ([Issue 1224](https://github.com/iBotPeaches/Apktool/issues/1224)) / Thanks BurgerZ
 * Restore `-d / --debug-mode` to simply change `android:debuggable` in `AndroidManifest.xml`. ([Issue 1235](https://github.com/iBotPeaches/Apktool/issues/1235)) / Thanks Benjamin-Dobell
 * Insert literal `versionName` if it is a reference to satisfy `aapt`. ([Issue 1234](https://github.com/iBotPeaches/Apktool/issues/1234)) / Thanks padlar
 * Fix Samsung apks that have an unknown 4 bytes. ([Issue 1131](https://github.com/iBotPeaches/Apktool/issues/1131))
 * Prevent manifest rename for Adobe AIR applications. ([Issue 1240](https://github.com/iBotPeaches/Apktool/issues/1240))

## v2.1.0
2016.03.27

 * **Breaking** - Removes SmaliDebugging feature. ([Issue 1061](https://github.com/iBotPeaches/Apktool/issues/1061))
 * Fixed issue with non printable chars in unknown files. Thanks ihanson
 * Fixed issue when a non-compressed file has no extension. ([Issue 1122](https://github.com/iBotPeaches/Apktool/issues/1122)) / Thanks BurgerZ
 * Added ability for launched executables (`aapt`) to differentiate between output and error streams. Thanks BurgerZ
 * Revamped internal storage of `apktool.yml` to be serialized objects vs entries in HashMap. ([Issue 1128](https://github.com/iBotPeaches/Apktool/pull/1128)) / Thanks rover
 * Closes streams that were not properly closed. ([Issue 1143](https://github.com/iBotPeaches/Apktool/issues/1143))
 * Fixes issue when `@null` was improperly decoded. ([Issue 1123](https://github.com/iBotPeaches/Apktool/issues/1123))
 * Fixes issue when apk filename has trailing space. ([Issue 1145](https://github.com/iBotPeaches/Apktool/issues/1145)) / Thanks BurgerZ
 * Fixes issue that all digits were treated as string using `\ ###` trick. ([Issue 1130](https://github.com/iBotPeaches/Apktool/issues/1130))
 * Added additional feature to `--keep-broken-res` to ignore resource duplicates. ([Issue 1164](https://github.com/iBotPeaches/Apktool/pull/1164)) / Thanks crpalmer
 * Performance enhancement - Stops using String.format() for `MISSING_RES_SPECS`. ([Issue 1186](https://github.com/iBotPeaches/Apktool/issues/1186)) / Thanks dnault
 * Added support for decoding `AndResGuard` apps. ([Issue 1170](https://github.com/iBotPeaches/Apktool/issues/1170))
 * Removed LittleEndianReader in favor for a public domain one. ([Issue 1166](https://github.com/iBotPeaches/Apktool/issues/1166)) / Thanks chirayudesai
 * Adapt 9patch decoder to handle any format (Color Table, RGB, RGBA, Gray, GrayAlpha). ([Issue 1180](https://github.com/iBotPeaches/Apktool/issues/1180)) / Thanks mattsarett

## v2.0.3
2015.12.31

 * **For developers** - Run `git submodule update --init --recursive` to setup submodules.
 * Fixed issue with too long command due to large amount of uncompressed files. ([Issue 1053](https://github.com/iBotPeaches/Apktool/issues/1053))
 * Fixed bad casting issue between `ResStringValue` and `ResAttr`. ([Issue 1060](https://github.com/iBotPeaches/Apktool/issues/1060))
 * Fixed bad casting issue between `ResStyleValue` and `ResAttr`. ([Issue 957](https://github.com/iBotPeaches/Apktool/issues/957), [Issue 1063](https://github.com/iBotPeaches/Apktool/issues/1063))
 * Prevent greedy additional `.dex` finder from pulling `.dex` files outside of apk root.
 * Move smali to git submodule for easier updates, update to `2.1.0` in process.
 * Fixed issue with echo in helper scripts. ([Issue 1056](https://github.com/iBotPeaches/Apktool/issues/1056))
 * Fixed issue with `mnc1` qualifier. ([Issue 1072](https://github.com/iBotPeaches/Apktool/issues/1072))
 * Fixed issue with apks that have a 28 byte `ResConfig` size. ([Issue 1084](https://github.com/iBotPeaches/Apktool/pull/1084)) / Thanks rover
 * Cleaned up code base to match AOSP naming. ([Issue 1099](https://github.com/iBotPeaches/Apktool/issues/1099))
 * Fixed issue with APKs that had sparse ResourceTable. ([Issue 964](https://github.com/iBotPeaches/Apktool/issues/964), [Issue 1031](https://github.com/iBotPeaches/Apktool/issues/1031))
 * Added support for `DATA_NULL_EMPTY`
 * Added support for API23 mnc values. They are no longer zero padded.
 * Fixed issue where large int values in `AndroidManifest.xml` were truncated due to overflow. ([Issue 767](https://github.com/iBotPeaches/Apktool/issues/767)) / Thanks gio73 and MarcMil
 * Added decode support for Dexguard Enterprise applications. ([Issue 1014](https://github.com/iBotPeaches/Apktool/issues/1014))
    * Simply creates dummy key value names to prevent duplicate resource error.

## v2.0.2
2015.10.12

 * [Migration Instructions from 2.0.1 to 2.0.2]({{ site.github.url }}/documentation/#v2-0-1-v2-0-2)
 * Fixed issues with apks that use `.9.xml` files, which improperly triggered 9patch decoder. ([Issue 1005](https://github.com/iBotPeaches/Apktool/issues/1005))
 * Prevent compressing resources that should not be. ([Pull 1020](https://github.com/iBotPeaches/Apktool/pull/1020))
 * `aapt` changes
    * [5cded813](https://github.com/iBotPeaches/platform_frameworks_base/commit/5cded8132294c860a374409b7e0c94167ab91e06) - skip compat functions.
    * [eb06229e](https://github.com/iBotPeaches/platform_frameworks_base/commit/eb06229e29362dded12f67cf0962f604e8214815) - add miui support for `godzillaui`.
    * [d3c5cc64](https://github.com/iBotPeaches/platform_frameworks_base/commit/d3c5cc64d686a95e40cd87682cef346a5b9eb352) - add miui support for 4 digit `mnc`/`mcc` fields.
    * [ef9e8d09](https://github.com/iBotPeaches/platform_frameworks_base/commit/ef9e8d86d0941cb80097f05274ec76fbdef2fbe7) - build `libc++` statically.
 * Updated smali/baksmali to `v2.0.8`
 * Fixed issues with reference attributes being decoded improperly. ([Issue 1023](https://github.com/iBotPeaches/Apktool/issues/1023)) / (Thanks phhusson)
 * Fixed issue with version qualifiers being improperly added during build. ([Issue 928](https://github.com/iBotPeaches/Apktool/issues/928))
 * Added Support for Android Marshmallow (API 23). ([Issue 999](https://github.com/iBotPeaches/Apktool/issues/999))

## v2.0.1
2015.07.15

 * Fixed version qualifier like `v4` from being ignored during decode. ([Issue 928](https://github.com/iBotPeaches/Apktool/issues/928))
 * Fixed windows helper script from appending current directory into `$PATH`. ([Issue 927](https://github.com/iBotPeaches/Apktool/issues/927)) / (Thanks Tercete)
 * Fixed frameworks that were SharedLibraries from affecting the `apktool.yml` file. ([Issue 936](https://github.com/iBotPeaches/Apktool/issues/936))
 * Fixed apks that were crashing on internal attributes. ([Issue 913](https://github.com/iBotPeaches/Apktool/issues/913))
 * Fixed `ResFileValue(s)` being casted to `ResScalarValues`. ([Issue 921](https://github.com/iBotPeaches/Apktool/issues/921))
 * Fixed reading `ResConfigFlags` twice. ([Issue 924](https://github.com/iBotPeaches/Apktool/issues/924))
 * Expose raw index used for resource lookups. ([Issue 990](https://github.com/iBotPeaches/Apktool/issues/990)) / (Thanks mmastrac)
 * Correctly add `libs` and `lib` folders on `[b]uild`
 
## v2.0.0
2015.04.21

 * [Migration Instructions from 1.5.x to 2.0.x]({{ site.github.url }}/documentation/#v1-5-x-v2-0-0)
 * **Android 5.1 support**
 * Updated smali/baksmali to `v2.0.5`
 * Updated gradle to `v2.1`
 * Fixed using `-c` to retain original manifest and META-INF folder. ([Issue 118](https://github.com/iBotPeaches/Apktool/issues/118))
 * Fixed handling apks that have unknown files outside of standard aapt allowed resources. ([Issue 174](https://github.com/iBotPeaches/Apktool/issues/174))
 * Fixed aapt incorrectly setting `pkgId`. ([Issue 313](https://github.com/iBotPeaches/Apktool/issues/313)) / (Thanks M1cha)
 * Added new usage output to organize features / parameters.  ([Issue 514](https://github.com/iBotPeaches/Apktool/issues/514))
 * Fixed NPE from malformed 9patch images. ([Issue 470](https://github.com/iBotPeaches/Apktool/issues/470)) / (Thanks Felipe Richards)
 * Fixed aapt requiring `versionName` and `versionCode` via parameter passing. ([Issue 512](https://github.com/iBotPeaches/Apktool/issues/512))
 * Fixed common `aapt` problems by including an internal mac, win and linux aapt. ([Issue 551](https://github.com/iBotPeaches/Apktool/issues/551))
 * Fixed decoding apks that had general access bit thrown. ([Issue 550](https://github.com/iBotPeaches/Apktool/issues/550))
 * Fixed debug mode (`-d`) to fix smali debugging. ([Issue 450](https://github.com/iBotPeaches/Apktool/issues/450)) / (Thanks Ryszard)
 * Adapted smali debugging output to make breakpoint setting easier across IDEs. ([Issue 228](https://github.com/iBotPeaches/Apktool/issues/288)) / (Thanks Ryszard)
 * Fixed characters (`&` & `<`) from being double escaped in `<item>`'s of `arrays.xml`. ([Issue 502](https://github.com/iBotPeaches/Apktool/issues/502))
 * Fixed "multiple substitution" errors with positional and exactly 1 non-positional argument. ([Issue 371](https://github.com/iBotPeaches/Apktool/issues/371))
 * Fixed ignoring `--frame-path` on `[b]`uild. ([Issue 538](https://github.com/iBotPeaches/Apktool/issues/538))
 * Fixed setting `android:debuggable` on debug apks. ([Issue 507](https://github.com/iBotPeaches/Apktool/issues/507))
 * Fixed common "superclass" errors on debug mode. ([Issue 451](https://github.com/iBotPeaches/Apktool/issues/451))
 * Fixed `pkgId` not being set in framework files. ([Issue 569](https://github.com/iBotPeaches/Apktool/issues/569))
 * Added `-m` / `--match-original` feature to allow apks to match original. ([Issue 580](https://github.com/iBotPeaches/Apktool/issues/580))
 * Fixed apks PNGs gaining brightness on rebuild. ([Issue 437](https://github.com/iBotPeaches/Apktool/issues/437))
 * Added dexlib2 (smali2) into Apktool. ([Issue 559](https://github.com/iBotPeaches/Apktool/issues/559))
 * Fixed windows builds caused by `java.nio`. ([Issue 606](https://github.com/iBotPeaches/Apktool/issues/606))
 * Fixed error output being written to `stdout` instead of `stderr`. ([Issue 620](https://github.com/iBotPeaches/Apktool/issues/620))
 * Fixed issue with smali filenames from being too long. ([Issue 537](https://github.com/iBotPeaches/Apktool/issues/537)) / (Thanks JesusFreke)
 * Fixed issue with `INSTALL_FAILED_DEXOPT`. ([Issue 634](https://github.com/iBotPeaches/Apktool/issues/634)) / (Thanks JesusFreke)
 * Fixed issue with apks with multiple packages. ([Issue 583](https://github.com/iBotPeaches/Apktool/issues/583))
 * Fixed issue with decoding `.jar` files. ([Issue 641](https://github.com/iBotPeaches/Apktool/issues/641))
 * Fixed issue with improperly labeling type of `<array>`'s. ([Issue 660](https://github.com/iBotPeaches/Apktool/issues/660))
 * Fixed issue with truncated strings. ([Issue 681](https://github.com/iBotPeaches/Apktool/issues/681)) / (Thanks jtmuhone)
 * Fixed issue with apks with multiple empty types via ignoring them. ([Issue 688](https://github.com/iBotPeaches/Apktool/issues/688))
 * Fixed issue with apks with one package named `android` from decoding. ([Issue 699](https://github.com/iBotPeaches/Apktool/issues/699))
 * Fixed StringBlock by making it thread safe. ([Issue 711](https://github.com/iBotPeaches/Apktool/issues/711)) / (Thanks aluedeke)
 * Fixed truncated `UTF-16` strings. ([Issue 349](https://github.com/iBotPeaches/Apktool/issues/349))
 * Spacing cleanup of 2014. ([Issue 694](https://github.com/iBotPeaches/Apktool/issues/694))
 * Fixed style crash due to malformed styles. ([Issue 307](https://github.com/iBotPeaches/Apktool/issues/307)) 
 * Fixed issue with unknown files being ignored that start with an accepted file name. ([Issue 713](https://github.com/iBotPeaches/Apktool/issues/713))
 * Fixed issue with unknown files being ignored when `-r` was used. ([Issue 716](https://github.com/iBotPeaches/Apktool/issues/716))
 * Fixed issue with renamed manifests such as (`android`, `com.htc` and `miui`). ([Issue 719](https://github.com/iBotPeaches/Apktool/issues/719))
 * Fixed path issues with `UTF8` chars and unknown files. ([Issue 736](https://github.com/iBotPeaches/Apktool/issues/736))
 * Fixed issue with renamed manifest (`com.lge`). ([Issue 740](https://github.com/iBotPeaches/Apktool/issues/740))
 * Fixed incorrect typing of `<array>` items due to incorrect loop index. ([Issue 520](https://github.com/iBotPeaches/Apktool/issues/520))
 * Fixed issue with `AndroidManifest.xml` missing attributes. ([Issue 623](https://github.com/iBotPeaches/Apktool/issues/623))
 * Fixed issue with ignoring `formatted="false"` attribute in `<string-array>`'s. ([Issue 786](https://github.com/iBotPeaches/Apktool/issues/786))
 * Fixed issue with multiple overlapping try catches. ([Issue 748](https://github.com/iBotPeaches/Apktool/issues/784))
 * Fixed issue with apks with multiple `ResPackages` where default is not `pkgId` 0. ([Issue 793](https://github.com/iBotPeaches/Apktool/issues/793))
 * Fixed issue with renamed manifest (`yi`). ([Issue 791](https://github.com/iBotPeaches/Apktool/issues/791))
 * Fixed issue with apks with large StringPools failing to decode. ([Issue 773](https://github.com/iBotPeaches/Apktool/issues/773))
 * Fixed issue with bad casting of `ResStringValue` to `ResAttr`. ([Issue 587](https://github.com/iBotPeaches/Apktool/issues/587)) / (Thanks whydoubt)
 * Fixed issue with hardcoding 9 patches as `.png` when there are `.qmg`, `.spi`. ([Issue 798](https://github.com/iBotPeaches/Apktool/issues/798))
 * Added support for Android 5.0 (Lollipop). ([Issue 763](https://github.com/iBotPeaches/Apktool/issues/763))
 * Added support for `TYPE_DYNAMIC_REFERENCE`. ([Issue 815](https://github.com/iBotPeaches/Apktool/issues/815))
 * Fixed issue with implicitly added version qualifiers. ([Issue 823](https://github.com/iBotPeaches/Apktool/issues/823))
 * Added support for shared library apks. ([Issue 822](https://github.com/iBotPeaches/Apktool/issues/822))
 * Fixed issue improperly casting strings that resembled filepaths to `ResFileValues`. ([Issue 440](https://github.com/iBotPeaches/Apktool/issues/440))
 * Fixed issue with segfaulting `aapt`. ([Issue 700](https://github.com/iBotPeaches/Apktool/issues/700))
 * Fixed issue with undefined attributes. ([Issue 655](https://github.com/iBotPeaches/Apktool/issues/655))
 * Fixed issue with improper handling of `MNC_ZERO` which caused duplicated resources. ([Issue 811](https://github.com/iBotPeaches/Apktool/issues/811))
 * Fixed warnings of "Cleaning up unclosed ZipFile...". ([Issue 853](https://github.com/iBotPeaches/Apktool/issues/853))
 * Added support for downloading gradle binaries over `https`. ([Issue 866](https://github.com/iBotPeaches/Apktool/issues/866))
 * Fixed issue when user has no access to `$HOME`. ([Issue 513](https://github.com/iBotPeaches/Apktool/issues/513))
 * Added support for `BCP-47` localization tags. ([Issue 870](https://github.com/iBotPeaches/Apktool/issues/870))
 * Fixed issue with double escaping of ampersands in `<`. ([Issue 658](https://github.com/iBotPeaches/Apktool/pull/105)) / (Thanks jhornber)
 * Fixed issue with not respecting compression type of unknown files. ([Issue 878](https://github.com/iBotPeaches/Apktool/issues/878)) / (Thanks simtel12) 
 * Fixed issue with apktool branding apks via `platformBuildVersion[Code/Name]`. ([Issue 890](https://github.com/iBotPeaches/Apktool/issues/890))
 * Fixed issue when multiple dex files were ignored using `-s`. ([Issue 904](https://github.com/iBotPeaches/Apktool/issues/904))
 * Fixed issue with `@string` references in `<provider>` attributes from preventing apk install. ([Issue 636](https://github.com/iBotPeaches/Apktool/issues/636))
 * Fixed issue with decoding `.spi` files as 9 patch images. (Thanks Furniel)
 * Fixed issue with APKs with multiple dex files. 
 * Fixed issue using Apktool without smali/baksmali.
 * Fixed issue using non URI standard characters in apk name. (Thanks rover12421)
 * Added version output during decode/build operations to quickly identify apktool version.
 * Fixed NPE error when using `.odex` files with `--no-src` specified. (Thanks Rodrigo Chiossi)
 * Fixed locale problems when locale changes meaning of windows `.bat` script. (Thanks Adem666)
 * Fixed issue when `-r` was used with no `/res` folder present. (Thanks chrisch1974)

## v1.5.2
2013.02.02

  * output smali filename errors to screen during rebuild instead of filestream ([Issue 410](https://github.com/iBotPeaches/Apktool/issues/410))
  * Only show the `--aapt / -a` info in verbose mode.
  * Don't crash out if .git folder isn't present. Use SNAPSHOT-DEV instead. ([Issue 503](https://github.com/iBotPeaches/Apktool/issues/503))
  * Only store compressed resources.arsc if original was compressed, otherwise STORE. ([Issue 178](https://github.com/iBotPeaches/Apktool/issues/178))
  * Moved build.gradle files to each sub-project for more organization
  * Prevented duplicated files in final jar which saved around 1.2mb. ([Issue 505](https://github.com/iBotPeaches/Apktool/issues/505))
  * Added Proguard to drop final jar size from 6.2mb to 2.6mb.
  * Added check for "aapt" in unit-tests. ([Issue 506](https://github.com/iBotPeaches/Apktool/issues/506))
  * Added ability to use `--frame-path` on `if|install-framework`
  * Fixed renaming of `.r.9.png` images that were incorrectly named to `.9.png`.
  * Added ability to use `--version` to print out Apktool version

## v1.5.1
2012.12.28

  * **Android 4.2 support**
  * Added -a / -aapt command on rebuild to specify location of aapt
  * Updated unit tests for 4.2 support
  * Closed file-handler when writing frameworks to file system.
  * Updated to Gradle 1.3
  * Properly deleted tmp files after building apk ([Issue 476](https://github.com/iBotPeaches/Apktool/issues/476))
  * Added support for renamed packages via `--renamed-manifest-package` ([Issue 363](https://github.com/iBotPeaches/Apktool/issues/363))
  * Option to specify framework folder ([Issue 286](https://github.com/iBotPeaches/Apktool/issues/286))
  * Prevents removal of configChanges in AndroidManifest ([Issue 415](https://github.com/iBotPeaches/Apktool/issues/415))
  * Updated snakeyaml to 1.11  to fix "unacceptable character" errors. ([Issue 471](https://github.com/iBotPeaches/Apktool/issues/471))
  * Updated smali/baksmali to `v1.4.1`
  * Fixed reference-array problem ( pull request [#53](https://github.com/iBotPeaches/Apktool/pull/53)))
  * Fixed bad spacing issue on Mac OS X (pull request [#49](https://github.com/iBotPeaches/Apktool/pull/49))
  * Removed maven in favor of gradle
  * Removed Maven REPOs that were used if local projects didn???t exist.
  * Merged brut.j.dir,brut.j.common,brut.j.util & brut.apktool.smali (Fork of JesusFreke???s smali) into one repo.
  * Fix ???verbose mode to actually work
  * Added SDK API 17 framework

## v1.5.0
2012.09.02

  * Fix for colours being decompiled with wrong hex code
  * Fix for `<string-array>` being treated as `<array>`
  * Support for Mac OS X user:home instead of /home
  * updated builtin framework to SDK API16
  * Added `<user-sdk>` into apktool.yml for future aapt changes
  * Added `--verbose` commands to output contents from aapt (help with debugging)
  * Ignore bootclasspath on debug mode

## v1.4.10
2012.08.21

  * Fix for bad whitespace in manifest
  * Fix for bad decompilation of some apks (Credit: KOJAN)

## v1.4.9
2012.07.28

  * Fix for plurals.xml (Credit: MIUIRussia)
  * Added xhdpi configurations
  * Added uimodes configurations - miui roms
  * Fixed problem escaping chars like `' /`

## v1.4.8
2012.07.08

  * Revert greyscale fix due to errors
  * Skip extra com.htc package in some apks.
  * Some fixes from yyj inserted

## v1.4.7
2012.07.05

  * updated to baksmali/smali to public `v1.3.3`
  * Fix for grayscaled images (Credit: Charles)
  * Adjusted resources/configurations for API13

## v1.4.6
2012.02.14

  * Fixed reading of xlif data to correctly insert `formatted="false"`
  * Fixed `<item>` being read incorrectly and placed as attr type

## v1.4.5
2012.01.07

  * updated builtin framework to SDK API15
  * updated baksmali/smali to `v1.3.3dev`

## v1.4.4
2011.12.11

  * updated baksmali/smali to `v1.3.3`
  * New developer: iBotPeaches

## v1.4.3
2011.12.08

  * updated builtin framework to SDK API14
  * fixed some `"Multiple substitutions (...)"` errors ([Issue 365](https://github.com/iBotPeaches/Apktool/issues/365))

## v1.4.2
2011.12.02

  * added support for API14 (Android 4.0) resources
  * updated smali to `v1.3.0`
  * added `--quiet` option
  * fixed decoding error when string ends with '%' ([Issue 280](https://github.com/iBotPeaches/Apktool/issues/280))
  * fixed decoding error when `<plurals>` contains a reference ([Issue 345](https://github.com/iBotPeaches/Apktool/issues/345))
  * fixed a broken res when decoding `<array>` with positional substitutions ([Issue 333](https://github.com/iBotPeaches/Apktool/issues/333))

## v1.4.1
2011.05.15

  * fixed builtin framework. See changelog and migration instructions of v1.4.0 below.

## v1.4.0
2011.05.15

  * added Honeycomb support (3.1, API 12).
    * support for mipmaps and xlarge, xhdpi resource qualifiers
    * updated builtin framework to 3.1 (API 12)
  * completely rewritten mechanism of enclosing/escaping strings in XML files:
    * fixed legendary [Issue 211](https://github.com/iBotPeaches/Apktool/issues/211)
    * fixed a lot of other bugs discovered when writing integration tests
    * string format is simpler and more compact now: `"  "` instead of `\u0020 `, `\"` instead of `\&quot;`, etc.
  * fixed incompatibilities between newer aapt and apks built by older one. New aapt is more restrictive, some apps can't be built using it, even if you would have sources. Apktool tries to convert/fix these incompatibilities: it adds formatted="false" for `<string />` tags and enumerates substitutions for plurals.
  * updated smali to `v1.2.6`
  * added automatic integration tests for resource decoding and building
  * first official release of apktool built using Maven from open source
  * sort framework ids before storing them in apktool.yml. aapt command requires you to include frameworks in order.
  * zero-padding of MCC resource qualifier
  * prefer to use raw values when decoding XML attrs. This could make decoded XMLs a little more similar to original ones.
  * close apktool.yml file handler after generating it
  * added error message about missing input file when decoding
  * added more info messages during decoding.
  * do not decode res-references as `<item />`. Now they're decoded as e.g. `<string name="test">@android:string/ok</string>` instead of `<item type="string" name="test">@android:string/ok</item>`.
  * changed encoding of generated XML files from UTF-8 to utf-8 - it's more consistent with Android SDK.
  * add new line at the end of generated XML files.

### Migration to 1.4.0

In order to get full Honeycomb/Gingerbread (3.1, API 12) support you have to:

  * update apktool to `v1.4.0`
  * update install package to `r04-brut1` or update your aapt manually
  * then remove `$HOME/apktool/framework/1.apk` or install your own framework from Honeycomb/Gingerbread

## v1.3.2
2010.09.03

  * contains critical bug: ([Issue 211](https://github.com/iBotPeaches/Apktool/issues/211)).
  * updated smali to `v1.2.4`
  * added support for API Level 8 resource qualifiers: night, car, etc. ([Issue 176](https://github.com/iBotPeaches/Apktool/issues/176))
  * added support for broken file-resources ([Issue 202](https://github.com/iBotPeaches/Apktool/issues/202))
  * don't generate sdkVersion (`"-v"`) resource qualifiers if they're "natural" ([Issue 196](https://github.com/iBotPeaches/Apktool/issues/196))
  * always compress resources.arsc file ([Issue 178](https://github.com/iBotPeaches/Apktool/issues/178))
  * throw warnings instead of exceptions on unknown files inside smali dir ([Issue 188](https://github.com/iBotPeaches/Apktool/issues/188))
  * added support for resources using invalid/unknown config flags, e.g. from future APIs or added by manufacturer ([Issue 176](https://github.com/iBotPeaches/Apktool/issues/176))
  * added an option to keep broken resources to fix them manually ([Issue 176](https://github.com/iBotPeaches/Apktool/issues/176))
  * fixed case-sensitivity problems ([Issue 197](https://github.com/iBotPeaches/Apktool/issues/197))
  * fixed an issue when `*`.9.png doesn't have 9patch chunk in it ([Issue 170](https://github.com/iBotPeaches/Apktool/issues/170))
  * fixed NPE when there is a file without extension in drawable dir ([Issue 173](https://github.com/iBotPeaches/Apktool/issues/173))
  * fixed escaping of chars in XML style tags ([Issue 175](https://github.com/iBotPeaches/Apktool/issues/175))
  * fixed an error, when there are missing resources in a type, which does not have default config (https://forum.xda-developers.com/showthread.php?p=7949440#post7949440)
  * try to use original value of XML attribute - instead of parsed one. Fixes an issue when apktool was decoding e.g. "01" as "1" ([Issue 187](https://github.com/iBotPeaches/Apktool/issues/187))
  * added more debugging info when omitting unknown config flags (`"Config size > 32" message`)

## v1.3.1
2010.06.14

  * added decoding of XML tags in res strings ([Issue 125](https://github.com/iBotPeaches/Apktool/issues/125))
  * fixed some issues ([Issue 155](https://github.com/iBotPeaches/Apktool/issues/155)), ([Issue 156](https://github.com/iBotPeaches/Apktool/issues/156)), ([Issue 158](https://github.com/iBotPeaches/Apktool/issues/158)), ([Issue 167](https://github.com/iBotPeaches/Apktool/issues/167))

## v1.3.0
2010.06.12

  * added 9patch images (`*`.9.png) decoding ([Issue 112](https://github.com/iBotPeaches/Apktool/issues/112))
  * fixed support for apks lacking res dir or resources.arsc file ([Issue 154](https://github.com/iBotPeaches/Apktool/issues/154), [Issue 160](https://github.com/iBotPeaches/Apktool/issues/160))
  * changed default name of built file from out.apk to `<original\_name.apk>`
  * added possibility to choose location of output apk when building

## v1.2.0
2010.06.03

  * added feature for installing and using custom framework files - pulled from a device. See FrameworkFiles ([Issue 137](https://github.com/iBotPeaches/Apktool/issues/137))
  * Froyo support ([Issue 147](https://github.com/iBotPeaches/Apktool/issues/147))
  * updated Android framework to `2.2r1`
  * removed HTC framework
  * no need to use `-s/-r` switch, when apk doesn't contain sources/resources
  * added protection against accidental remove of important files when decoding ([Issue 146](https://github.com/iBotPeaches/Apktool/issues/146))
  * made outdir argument optional when decoding
  * fix: adding dummy resources if some of them are missing ([Issue 150](https://github.com/iBotPeaches/Apktool/issues/150))
  * fix: better recognition of AXML files ([Issue 151](https://github.com/iBotPeaches/Apktool/issues/151))

## v1.1.1
2010.04.29

  * much better recognition of register types when debugging ([Issue 134](https://github.com/iBotPeaches/Apktool/issues/134))
  * fixed SIGSEGV error, which usually occurred after several steps when debugging ([Issue 136](https://github.com/iBotPeaches/Apktool/issues/136))

## v1.1.0
2010.04.28

  * added smali debugging! For more info, see: SmaliDebugging
  * added HTC resources ([Issue 127](https://github.com/iBotPeaches/Apktool/issues/127))
  * made all framework resources public ([Issue 126](https://github.com/iBotPeaches/Apktool/issues/126))
  * proper escaping of whitespaces in resource strings ([Issue 124](https://github.com/iBotPeaches/Apktool/issues/124))
  * updated (bak)smali to 1.2.2
  * fixed "Building resources..." freeze bug ([Issue 123](https://github.com/iBotPeaches/Apktool/issues/123))

## v1.0.0
2010.04.02

  * it is now pure-Java, so should work on any platform
  * added support for decoding and rebuilding framework-res.apk file
  * added support for many new resources features and apks
  * included automatic workaround for 9-patch images issue
  * added possibility to decode sources or resources only
  * automatic detecting, whether there is a need for rebuilding files
  * added some info messages
  * it is less invasive, cause res ids in built file are identical as in original apk
  * it is much faster
  * fixed a lot of bugs

## v0.9.2
2010.03.13

  * many, many new apps supported. I've tested it on 85 random apps pulled from my device: 0.9.1 gave me 28 failures, 0.9.2 only 2. This does not mean all 83 apps are perfectly fine, but it is quite probably that they are.
  * smali, baksmali and android resources are now builtin, so it is much simpler to install apktool. Still you need aapt in a PATH.
  * much better error reporting
  * added simple usage help
  * new "bs" command

## v0.9.1
2010.03.02

  * [#111](https://github.com/iBotPeaches/Apktool/issues/111) fixed
  * fixed support for many apps
