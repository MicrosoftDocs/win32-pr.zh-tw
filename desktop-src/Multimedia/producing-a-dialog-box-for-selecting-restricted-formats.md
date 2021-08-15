---
title: 產生對話方塊來選取限制的格式
description: 產生對話方塊來選取限制的格式
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- 音訊壓縮管理員 (的) 、產生對話方塊
- " (音效壓縮管理員) 、產生對話方塊"
- 進行中的範例，產生對話方塊
- 產生對話方塊
- acmFormatChoose 函式
- 音訊壓縮管理員 (的) ，選取受限制的格式
- " (音效壓縮管理員) ，選取受限格式"
- 未通過範例，選取受限制的格式
- 選取限制的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994fffa7ef13f6febe41eb766b4ecaef7eb735f11f58d36f37adfccbb152bffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802038"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>產生對話方塊來選取限制的格式

您可能會想要使用 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) 函式所建立的對話方塊，但限制或控制對話方塊中的格式。 若要這樣做，您可以使用 ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK 旗標來攔截對話程式。 然後，應用程式可以藉由回應對話方塊的訊息程式中的 [**MM \_ \_ FORMATCHOOSE**](mm-acm-formatchoose.md) 訊息來篩選格式。

 

 




