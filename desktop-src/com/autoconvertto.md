---
title: AutoConvertTo
description: 指定將物件的指定類別自動轉換成物件的新類別。
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- AutoConvertTo 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839068"
---
# <a name="autoconvertto"></a>AutoConvertTo

指定將物件的指定類別自動轉換成物件的新類別。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值，可指定物件的類別識別碼，該物件為物件的指定物件或類別應轉換成的物件。

此索引鍵通常用來將繼承應用程式所建立的檔案，自動轉換為較新版本的應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




