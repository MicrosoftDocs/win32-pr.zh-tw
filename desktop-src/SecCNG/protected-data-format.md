---
description: 受保護的資料會儲存為 asn.1 編碼的 BLOB。
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: 受保護的資料格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b4985fee02b5c40b9ad51a6645c4e0d9894a358a871c2067e44dd5f90da26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907402"
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

 

 



