---
title: TreatAs
description: 指定可模擬目前類別之類別的 CLSID。
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- TreatAs 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840283"
---
# <a name="treatas"></a>TreatAs

指定可模擬目前類別之類別的 CLSID。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值。

模擬可以讓某個應用程式開啟和編輯不同類別的物件，同時保留物件的原始格式。 解析發生在本機電腦上，因此在遠端啟動案例中，解析會在用戶端電腦上使用 **TreatAs** 所指定的 CLSID 進行。

DCOM 會查看 **TreatAs** 的本機登錄，即使您呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數並指定遠端伺服器也一樣。 這表示，如果您有要在本機電腦上將 Class1 視為 Class2 的 **TreatAs** 專案，但您呼叫 **CoCreateInstance** 來建立 Class1 的實例，並指定遠端伺服器，則 DCOM 將會嘗試在遠端伺服器上建立 Class2 的實例，即使 Class2 未在遠端伺服器上註冊，也會導致對 **CoCreateInstance** 的呼叫失敗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AutoTreatAs**](autotreatas.md)
</dt> <dt>

[**CoGetTreatAsClass**](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




