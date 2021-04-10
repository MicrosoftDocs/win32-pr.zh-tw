---
title: 語音辨識引擎的需求
description: 語音辨識引擎的需求
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932465"
---
# <a name="requirements-for-speech-recognition-engines"></a><span data-ttu-id="de9ee-103">語音辨識引擎的需求</span><span class="sxs-lookup"><span data-stu-id="de9ee-103">Requirements for Speech Recognition Engines</span></span>

<span data-ttu-id="de9ee-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="de9ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="de9ee-105">語音辨識引擎也必須是完全符合規範的命令和控制 (C&C) 引擎（根據 SAPI 4.0）。</span><span class="sxs-lookup"><span data-stu-id="de9ee-105">A speech recognition engine must also be a fully compliant Command and Control (C&C) engine according to SAPI 4.0.</span></span> <span data-ttu-id="de9ee-106">它必須支援規格中所描述之二進位格式的多個文法，並允許即時啟用或停用這些文法。</span><span class="sxs-lookup"><span data-stu-id="de9ee-106">It must support multiple grammars in the binary format described in the specification and allow those grammars to be activated or deactivated in real time.</span></span>

<span data-ttu-id="de9ee-107">請注意，若要讓語音辨識引擎支援寬字元、Unicode 介面，則必須支援 SAPI 4.0。</span><span class="sxs-lookup"><span data-stu-id="de9ee-107">Note that SAPI 4.0 requires that speech recognition engines support the wide character, Unicode interfaces.</span></span> <span data-ttu-id="de9ee-108">不過，在支援這些介面時，引擎不應該相依于將 Unicode 資料轉換成 ANSI，因為引擎可能無法在某些系統上正確運作。</span><span class="sxs-lookup"><span data-stu-id="de9ee-108">However, in supporting these interfaces, the engine should not depend on converting Unicode data to ANSI, as the engine may not function correctly on some systems.</span></span> <span data-ttu-id="de9ee-109">例如，將 Unicode 轉換成 ANSI 的日文引擎可能無法在英文 Microsoft Windows 95 系統上運作。</span><span class="sxs-lookup"><span data-stu-id="de9ee-109">For example, a Japanese engine that converts Unicode to ANSI may not work on an English-language Microsoft Windows 95 system.</span></span>

<span data-ttu-id="de9ee-110">此外，若要將它視為符合 Microsoft 代理程式規範，引擎必須在成功辨識片語 (透過 ISRGramNotifySinkW：:P hraseFinish) 傳回結果物件。</span><span class="sxs-lookup"><span data-stu-id="de9ee-110">In addition, to be considered Microsoft Agent-compliant, the engine must return results objects upon the successful recognition of a phrase (through ISRGramNotifySinkW::PhraseFinish).</span></span> <span data-ttu-id="de9ee-111">這些結果物件必須支援 ISRResBasic，如規格所要求。</span><span class="sxs-lookup"><span data-stu-id="de9ee-111">These results objects must support ISRResBasic, as the specification requires.</span></span> <span data-ttu-id="de9ee-112">此外，它們也應支援 ISRResScore。</span><span class="sxs-lookup"><span data-stu-id="de9ee-112">In addition, they should support ISRResScore.</span></span> <span data-ttu-id="de9ee-113">雖然 Microsoft Agent 會使用僅支援 ISRResBasic 的引擎來執行，或甚至是在不傳回任何結果物件的引擎的情況下執行，但效能通常會明顯地與這類引擎較差。</span><span class="sxs-lookup"><span data-stu-id="de9ee-113">Although Microsoft Agent will run with an engine that supports only ISRResBasic, or even with an engine that returns no results objects whatsoever, performance will usually be significantly poorer with such engines.</span></span> <span data-ttu-id="de9ee-114">許多應用程式都使用引擎所提供的信賴價值來控制它們回應各種命令的方式。</span><span class="sxs-lookup"><span data-stu-id="de9ee-114">Many applications use the confidence values provided by the engine to control how they respond to various commands.</span></span>

 

 




