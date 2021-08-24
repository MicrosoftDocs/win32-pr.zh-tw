---
description: 當您將資料庫當地語系化時，必須將摘要資訊資料流程中的 [修訂編號摘要] 屬性值變更為新的唯一值，因為安裝資料庫已變更。 請參閱套件代碼。
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: 更新摘要資訊資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d95e6a0cf09af5d4a024f707c0694d89def47abf8f731f394c55a11232bc07f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039278"
---
# <a name="updating-a-summary-information-stream"></a>更新摘要資訊資料流程

當您將資料庫當地語系化時，必須將 [摘要資訊資料流程](summary-information-stream.md)中的 [[**修訂編號摘要**](revision-number-summary.md)] 屬性值變更為新的唯一值，因為安裝資料庫已變更。 請參閱 [套件代碼](package-codes.md)。

您必須將摘要資訊資料流程中 [**範本摘要**](template-summary.md) 屬性的值變更為新語言 (LANGID) 的數值語言識別項。

如果摘要資訊資料流程中的描述性文字字串已當地語系化為新的語言，則必須將 [字碼頁 [**摘要**](codepage-summary.md) ] 屬性設定為新語言的正確字碼頁。

您可以依照 [新增摘要資訊](adding-summary-information.md)中的相同程式，修改當地語系化封裝的摘要資訊資料流程。 Windows Installer SDK 中也提供示範資料庫摘要資訊方法使用方式的範例，作為公用程式 WiSumInf.vbs。 如需 WiSumInf.vbs 的詳細資訊，請參閱 [管理摘要資訊](manage-summary-information.md)。

[繼續](adding-localized-resources.md)

 

 



