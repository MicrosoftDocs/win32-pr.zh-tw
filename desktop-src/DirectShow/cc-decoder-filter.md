---
description: CC 解碼篩選
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: CC 解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935696"
---
# <a name="cc-decoder-filter"></a>CC 解碼篩選

> [!IMPORTANT]
> 此元件已從 Windows Vista 和更新版本的作業系統中移除。 它可在 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用。

 

CC VBI 解碼器是核心模式資料流程類別篩選。 它會顯示在 GraphEdit 的 [WDM 串流 VBI 編解碼器] 類別之下。 它接受 capture 篩選器所提供的範例波形，並將解碼的封閉字幕資料傳遞到 [第21行的解碼器](line-21-decoder-filter.md) 和/或感興趣的應用程式。

此篩選器有兩個輸入圖釘： VBI 和 HWCC。 VBI 的 pin 會用於原始的 VBI 資料，而 HWCC 的 pin 會在使用 capture 篩選器在硬體中執行 VBI 解碼時使用。 在 HWCC 的 pin 上收到資料時，CC 解碼會以「通過」模式運作，並將資料直接傳送到第21行的解碼器，而不需要以任何方式處理。 如果捕捉篩選器公開 HWCC 的 pin，則必須直接連接到 CC 解碼器上的對應 pin。 Pin 類別為 **PINNAME \_ VIDEO \_ CC \_ CAPTURE**。

CC 解碼最多可有八個輸出圖釘，每個輸出都可以選取自己的行和子串流。 第一個輸出連接會連接到第21行的解碼器。

CC 編碼器篩選器會出現在 [WDM 串流 VBI 編解碼器] 篩選類別中， (**AM \_ KSCATEGORY \_ VBICODEC**) 。

由於這是核心模式篩選器，因此應用程式無法直接使用 **CoCreateInstance** 來建立它。 相反地，請使用 [系統裝置枚舉器](system-device-enumerator.md)。 如需詳細資訊，請參閱 [建立 Kernel-Mode 篩選](creating-kernel-mode-filters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[查看隱藏式輔助字幕](viewing-closed-captions.md)
</dt> </dl>

 

 



