---
title: 語音辨識引擎的需求
description: 語音辨識引擎的需求
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1315d395e3053d5f6f71fd7f8ff17cb815bea26fc4875878da74dd77113d5e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975748"
---
# <a name="requirements-for-speech-recognition-engines"></a>語音辨識引擎的需求

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

語音辨識引擎也必須是完全符合規範的命令和控制 (C&C) 引擎（根據 SAPI 4.0）。 它必須支援規格中所描述之二進位格式的多個文法，並允許即時啟用或停用這些文法。

請注意，若要讓語音辨識引擎支援寬字元、Unicode 介面，則必須支援 SAPI 4.0。 不過，在支援這些介面時，引擎不應該相依于將 Unicode 資料轉換成 ANSI，因為引擎可能無法在某些系統上正確運作。 例如，將 Unicode 轉換成 ANSI 的日文引擎可能無法在英文 Microsoft Windows 95 系統上運作。

此外，若要將它視為符合 Microsoft 代理程式規範，引擎必須在成功辨識片語 (透過 ISRGramNotifySinkW：:P hraseFinish) 傳回結果物件。 這些結果物件必須支援 ISRResBasic，如規格所要求。 此外，它們也應支援 ISRResScore。 雖然 Microsoft Agent 會使用僅支援 ISRResBasic 的引擎來執行，或甚至是在不傳回任何結果物件的引擎的情況下執行，但效能通常會明顯地與這類引擎較差。 許多應用程式都使用引擎所提供的信賴價值來控制它們回應各種命令的方式。

 

 




