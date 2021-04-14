---
title: 產生對話方塊來選取錄製的格式
description: 產生對話方塊來選取錄製的格式
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- 音訊壓縮管理員 (的) 、產生對話方塊
- " (音效壓縮管理員) 、產生對話方塊"
- 進行中的範例，產生對話方塊
- 產生對話方塊
- acmFormatChoose 函式
- 音訊壓縮管理員 (的) ，選取用於編碼的格式
- " (的音訊壓縮管理員) ，選取用於編碼的格式"
- 未通過範例，選取用於編碼的格式
- 選取用於編碼的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/27/2020
ms.locfileid: "104374673"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a>產生對話方塊來選取錄製的格式

應用程式可讓使用者選取已安裝的波形音訊裝置提供原生支援的格式。 例如，您可能想要讓波形音訊編輯器錄製新的波形音訊資料，而不使用高階的壓縮程式或解壓縮程式來提供轉譯層。 若要這樣做，請使用 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose)函式， \_ \_ \_ \_ 在 [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)結構的 **fdwEnum** 成員中指定 [執行類型 FORMATENUMF 硬體] 和 [執行識別碼] FORMATENUMF 輸入旗標。

 

 




