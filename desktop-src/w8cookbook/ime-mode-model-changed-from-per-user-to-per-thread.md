---
title: IME 模式模型變更
description: 輸入法模式模型從每位使用者變更為每個執行緒
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443244"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>輸入法模式模型從每位使用者變更為每個執行緒

## <a name="platforms"></a>平台

<dl> 用戶端-Windows 8。1  
伺服器-Windows Server 2012 R2  
</dl>

## <a name="description"></a>描述

在 Windows 8 中，IME 轉換模式與輸入法（IME）模式是以使用者內容為基礎，而變更應用程式的模式會影響所有其他應用程式。 您可以使用語言 [控制台] 的 [advanced settings] 區段中的 [讓我為每個應用程式視窗設定不同的輸入方法] 設定，來停用此行為。

為了改善相容性，Windows 8.1 模式會儲存在輸入內容中，而不論「讓我為每個應用程式設定不同的輸入方法」控制項的設定為何。 在 Windows 8.1 中，「讓我為每個應用程式視窗設定不同的輸入方法」設定只會影響輸入方法本身的選取專案。

在應用程式啟動時，IME 模式會設定為下列預設值：



| &nbsp;   | 軟體輸入面板 | 硬體鍵盤 |
|----------|----------------------|-------------------|
| KOR、JPN | 開啟                   | 關閉               |
| CHS、CHT  | 開啟                   | 開啟                |



 

## <a name="manifestations"></a>表現

當使用者變更應用程式的 IME 模式時，變更不會影響其他應用程式。

## <a name="resources"></a>資源

-   [IME 轉換模式值](../intl/ime-conversion-mode-values.md)
-   [IME 句子模式值](../intl/ime-sentence-mode-values.md)

 

 