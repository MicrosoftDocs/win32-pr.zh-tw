---
title: 從檔案讀取
description: 從檔案讀取
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95186b1ec8913623b0ab02e0d2bc5556302d4dcd03f7737ac12c5872b9f2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371681"
---
# <a name="reading-from-a-file"></a>從檔案讀取

您可以使用 [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) 函式來取得開啟檔案的相關資訊。 此函式會使用這類資訊來填滿 [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) 結構，包括最大資料速率、檔案中的資料流程數目、檔案是否使用索引，以及檔案是否受保護。

若要取得 AVI 檔案中的補充資訊，請使用 [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) 函數。 補充資訊適用于整個檔案，而且不會包含在一般檔案標頭中。 例如，持有檔案著作權的公司或人員名稱可能是補充資訊。 補充資訊不遵守特定格式;它可以是檔案特定的。 **AVIFileReadData** 會在應用程式提供的緩衝區中傳回補充資訊。

 

 




