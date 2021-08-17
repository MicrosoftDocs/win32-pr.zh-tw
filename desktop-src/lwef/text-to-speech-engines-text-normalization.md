---
title: 文字轉換語音引擎文字正規化
description: 文字轉換語音引擎文字正規化
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd195212d52d9107aa8112c156bfd8dd6b33d00d2161bec624d182f0f12f78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347918"
---
# <a name="text-to-speech-engines-text-normalization"></a>文字轉換語音引擎文字正規化

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

正規化是識別數位、縮寫、縮寫和 idiomatics，並視需要將它們轉換成全文檢索的程式（通常是根據句子的內容）。

例如，使用 L&H TruVoice 美式英文 TTS 引擎（句子：

1952年2月6日的王 George VI 壞掉。

將在 **正常內容** 下讀取，如下所示：

   19 52 年2月6日壞掉的王 George V

但是在 [ **電子郵件內容**] 下，它將會讀取如下：

   王 George，壞掉于 19 52 年2月6日。

您可以在代理程式程式設計檔 [Microsoft Agent 語音輸出標記](microsoft-agent-speech-output-tags.md)中找到使用 **內容** 聲控標籤的相關資訊。

 

 




