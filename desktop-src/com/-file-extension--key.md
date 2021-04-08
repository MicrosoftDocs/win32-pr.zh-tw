---
title: file_extension 金鑰
description: 將副檔名與 ProgID 產生關聯。
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840795"
---
# <a name="file_extension-key"></a><\_ 副檔名> 金鑰

將副檔名與 ProgID 產生關聯。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>備註

副檔名中包含的資訊是由 Windows 檔案總管和檔案的名字標記所使用。 [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) 使用副檔名來提供相關聯的 CLSID。

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**FileType**](filetype-key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




