---
title: DataFormats
description: 指定應用程式所支援的預設和主要資料格式。
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- DataFormats 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb8b2cc2ad4d11137fa41f419db2184f1a2b47fb850176227401e3d2b1aec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310596"
---
# <a name="dataformats"></a>DataFormats

指定應用程式所支援的預設和主要資料格式。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a>備註

檔案 */格式* 值會指定這個類別之物件的預設主要檔案或物件格式。

[ *格式* ] 值會指定 [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)預設實值的格式清單，其中 *n* 是以零為基礎的整數索引。 例如，[ *n* 格式]、[外觀]、[中]、[旗標]、[格式] 是 [剪貼簿] 格式、[中] 是一或多個 >dvaspect 成員、[中] 是一或多個  =     [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)成員，而 *旗* 標是 [](/windows/win32/api/wtypes/ne-wtypes-dvaspect)一個或多個   [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IDataObject：： EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject：：：：的**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject：： SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




