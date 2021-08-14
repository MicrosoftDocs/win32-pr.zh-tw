---
title: 變更範例音訊 DSP 外掛程式屬性
description: 變更範例音訊 DSP 外掛程式屬性
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，音訊屬性
- DSP 外掛程式、音訊屬性
- 音訊 DSP 外掛程式，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8aac1cf385f41e966bec51f19454308cf52697c995db4962a45486999ebae9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342621"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>變更範例音訊 DSP 外掛程式屬性

您可能會想要變更 Windows Media Player 外掛程式 Wizard 預設建立的屬性。 下列清單詳細說明可能需要變更的專案：

-   **對話方塊資源。** 按一下 [Project 工作區] 視窗中的 [ **ResourceView** ] 索引標籤。 展開資料夾清單以開啟對話方塊資料夾。 按兩下對話方塊資源以開啟資源編輯器。 您可以對 [屬性頁] 對話方塊進行變更，以滿足您的需求。 例如，您可以變更標籤中的文字，或以核取方塊取代編輯控制項。
-   **屬性頁物件程式碼。** 預設的執行會使用類型為 double 的變數來儲存比例因數。 您可能需要不同類型的資料。 這也需要您變更將資料保存到登錄的程式碼，並從登錄中讀取資料 (包括從 *CProjectName*：：**FinalConstruct**) 中的登錄讀取的程式碼。
-   **儲存屬性值的成員變數。** 此變數命名為 "m \_ fScaleFactor"，並宣告為 double 類型。 您可能會想要在整個專案中變更這個變數的名稱和類型。
-   **屬性 get 和屬性 put 方法。** 您可能會想要變更這些方法的名稱、參數和執行方式。 別忘了也在專案中的其他地方反映這些變更。 例如， **屬性頁會** 套用方法呼叫 *CProjectName*：：**put \_ 小** 數位數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行音訊 DSP 外掛程式**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




