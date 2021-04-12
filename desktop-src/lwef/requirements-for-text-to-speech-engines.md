---
title: 文字轉換語音引擎的需求
description: 文字轉換語音引擎的需求
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462257"
---
# <a name="requirements-for-text-to-speech-engines"></a><span data-ttu-id="37eef-103">文字轉換語音引擎的需求</span><span class="sxs-lookup"><span data-stu-id="37eef-103">Requirements for Text-To-Speech Engines</span></span>

<span data-ttu-id="37eef-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="37eef-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="37eef-105">引擎必須完全符合 SAPI 4.0 規範。</span><span class="sxs-lookup"><span data-stu-id="37eef-105">The engine must be fully SAPI 4.0-compliant.</span></span> <span data-ttu-id="37eef-106">此外，引擎也必須支援下列用於標記文字和書簽通知的 SAPI 介面。</span><span class="sxs-lookup"><span data-stu-id="37eef-106">In addition, the engine must also support the following SAPI interfaces for tagged text and bookmark notifications.</span></span> <span data-ttu-id="37eef-107">這些介面可讓 Microsoft 代理程式將文字輸出的步調和字元的字組文字提示保持一致，並將字元的嘴 (或對等的) 與說話的單字進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="37eef-107">These interfaces enable Microsoft Agent to pace the output of text to a character's word balloon and lip-sync the character's mouth (or equivalent) with the spoken words.</span></span>

-   [<span data-ttu-id="37eef-108">ITTSCentralW</span><span class="sxs-lookup"><span data-stu-id="37eef-108">ITTSCentralW</span></span>](ittscentralw.md)
-   [<span data-ttu-id="37eef-109">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="37eef-109">ITTSNotifySinkW</span></span>](ittsnotifysinkw.md)
-   [<span data-ttu-id="37eef-110">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="37eef-110">ITTSBufNotifySinkW</span></span>](ittsbufnotifysinkw.md)
-   [<span data-ttu-id="37eef-111">ITTSAttributesW</span><span class="sxs-lookup"><span data-stu-id="37eef-111">ITTSAttributesW</span></span>](ittsattributesw.md)

 

 




