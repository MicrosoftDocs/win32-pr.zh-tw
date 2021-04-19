---
title: /version_stamp 參數
description: /Version \_ 戳記參數會隱藏指定 RPC 標頭檔的最小必要版本號碼 Rpcndr .h 的宏產生。
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp switch MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106994952"
---
# <a name="version_stamp-switch"></a>/version \_ 戳記參數

**/Version \_ 戳記** 參數會隱藏指定 RPC 標頭檔的最小必要版本號碼 Rpcndr .h 的宏產生。

新的 MIDL 功能可能需要額外的定義，才能正確編譯存根，因此存根有宏可檢查 MIDL 二進位檔和組建環境之間的相容性。 如果您將 MIDL 移至與您第一次安裝 MIDL 二進位檔案的不同的組建環境，您可能需要使用這個參數。

請注意，不支援混合組建環境。

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

 

 




