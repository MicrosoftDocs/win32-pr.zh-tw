---
title: 設定自訂任意資料流程
description: 設定自訂任意資料流程
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- 串流，設定自訂任意資料流程
- 編解碼器，設定自訂任意資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b98b25ae9f973682ee3987ed8b590d485288e72e0b5ef7977eb7f3da0d1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809808"
---
# <a name="configuring-custom-arbitrary-streams"></a>設定自訂任意資料流程

使用您自己的任意資料類型時，您必須建立 GUID 值做為它的主要媒體類型識別碼。 當寫入器遇到具有無法辨識之主要類型的設定檔中的資料流程時，它會假設資料流程是自訂的任意資料。 它會接受您的範例、packetize 它們，並將它們與檔案中其他資料流程的範例合併，而不需要以任何方式驗證資料。

您也可以建立自己的子類型 GUID 識別碼，來定義自訂資料的子類別。 寫入器會完全忽略這些子類型，但會保留在 ASF 檔案的標頭區段中，讓您的讀取應用程式可以取出這些子類型，並根據它們進行決策。

任意的資料流程需要位元速率和緩衝區視窗，而且必須具有已清除值的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構，但主要媒體類型和子類型除外 (如果使用一個) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定任意資料流程類型**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**自訂任意資料流程**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




