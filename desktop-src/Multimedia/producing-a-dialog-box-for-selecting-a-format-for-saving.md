---
title: 產生對話方塊來選取儲存格式
description: 產生對話方塊來選取儲存格式
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- 音訊壓縮管理員 (的) 、產生對話方塊
- " (音效壓縮管理員) 、產生對話方塊"
- 進行中的範例，產生對話方塊
- 產生對話方塊
- acmFormatChoose 函式
- 音訊壓縮管理員 (的) ，選取儲存格式
- " (音效壓縮管理員) ，選取儲存格式"
- 進行中的範例，選取儲存格式
- 選取儲存格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/27/2020
ms.locfileid: "104374676"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a>產生對話方塊來選取儲存格式

您可能想要讓應用程式以另一種格式儲存現有的波形音訊資料。 例如，波形音訊編輯器可能會將波形音訊檔案儲存為壓縮檔案。 若只要針對 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose)函式所建立之對話方塊中的指定來源格式，只列出建議的目的地格式，請在 **pwfxEnum** 成員中指定來源格式，並 \_ 在 \_ [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)結構的 **fdwEnum** 成員中指定 [] FORMATENUMF 建議旗標。

同樣地，若要列出指定格式的有效目的地格式，請使用 [未執行] \_ FORMATENUMF \_ 轉換旗標，而不是 [執行 \_ FORMATENUMF \_ 建議] 旗標。

 

 




