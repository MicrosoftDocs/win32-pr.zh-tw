---
description: 受保護的資料會儲存為 asn.1 編碼的 BLOB。
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: 受保護的資料格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115184"
---
# <a name="protected-data-format"></a>受保護的資料格式

受保護的資料會儲存為 asn.1 編碼的 BLOB。 資料會格式化為 CMS (憑證訊息語法) 封包的內容。 數位信封包含加密的內容、包含加密內容加密金鑰 (CEK) 的收件者資訊，以及包含內容相關資訊的標頭（包括未加密的保護描述項規則字串）。 如下圖所示。

![受保護的封包資料](images/protecteddatablob.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[保護描述項](protection-descriptors.md)
</dt> <dt>

[保護提供者](protection-providers.md)
</dt> </dl>

 

 



