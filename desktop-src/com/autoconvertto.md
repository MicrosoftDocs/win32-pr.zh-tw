---
title: AutoConvertTo
description: 指定將物件的指定類別自動轉換成物件的新類別。
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- AutoConvertTo 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ea2b32445bb7107dcbfdc2aec8aee518fdd474674e76fdbd820265d06b6160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097048"
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

 

 




