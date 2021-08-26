---
title: 私人線上商店
description: 私人線上商店
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player 線上商店，私用
- 線上商店，私用
- 輸入1個線上商店，私用
- 輸入2個線上商店，私用
- 私人線上商店
- 登錄，私人線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0667c19ffde3bb3c78b539253650e4f6f0b84cfbfd940f4d06237f987b99efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002928"
---
# <a name="private-online-stores"></a>私人線上商店

Windows Media Player 10 或更新版本支援私人線上商店;也就是說，只有特定使用者才會看到存放區。 若要讓目前的使用者看見私人線上商店，您必須在下列登錄機碼底下輸入代表私人線上商店的專案。

HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ PrivateServices

必要的登錄專案必須具有下列格式。



| 名稱                                                         | 類型           | 值                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| 建立登錄專案的人員所選擇的任何名稱 | **REG \_ DWORD** | 由 Microsoft 提供的數位，可識別私人線上商店 |



 

只有當控制項在遠端模式中執行時，Windows Media Player 10 ActiveX 控制項才支援私用線上存放區。 無論控制項是否以遠端模式執行，Windows Media Player 11 ActiveX 控制項都支援私用線上商店。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




