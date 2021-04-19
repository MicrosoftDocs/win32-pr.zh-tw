---
title: DataFormats
description: 指定應用程式所支援的預設和主要資料格式。
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- DataFormats 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969676"
---
# <a name="dataformats"></a><span data-ttu-id="6e461-104">DataFormats</span><span class="sxs-lookup"><span data-stu-id="6e461-104">DataFormats</span></span>

<span data-ttu-id="6e461-105">指定應用程式所支援的預設和主要資料格式。</span><span class="sxs-lookup"><span data-stu-id="6e461-105">Specifies the default and main data formats supported by an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6e461-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="6e461-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a><span data-ttu-id="6e461-107">備註</span><span class="sxs-lookup"><span data-stu-id="6e461-107">Remarks</span></span>

<span data-ttu-id="6e461-108">檔案 */格式* 值會指定這個類別之物件的預設主要檔案或物件格式。</span><span class="sxs-lookup"><span data-stu-id="6e461-108">The *file/format* value specifies the default main file or object format for objects of this class.</span></span>

<span data-ttu-id="6e461-109">[ *格式* ] 值會指定 [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)預設實值的格式清單，其中 *n* 是以零為基礎的整數索引。</span><span class="sxs-lookup"><span data-stu-id="6e461-109">The *formats* value specifies a list of formats for default implementations of [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), where *n* is a zero-based integer index.</span></span> <span data-ttu-id="6e461-110">例如，[ *n* 格式]、[外觀]、[中]、[旗標]、[格式] 是 [剪貼簿] 格式、[中] 是一或多個 >dvaspect 成員、[中] 是一或多個  =     [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)成員，而 *旗* 標是 [](/windows/win32/api/wtypes/ne-wtypes-dvaspect)一個或多個   [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir)</span><span class="sxs-lookup"><span data-stu-id="6e461-110">For example, *n* = *format*, *aspect*, *medium*, *flag*, where *format* is a clipboard format, *aspect* is one or more members of [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* is one or more members of [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), and *flag* is one or more members of [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e461-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e461-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e461-112">**IDataObject：： EnumFormatEtc**</span><span class="sxs-lookup"><span data-stu-id="6e461-112">**IDataObject::EnumFormatEtc**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[<span data-ttu-id="6e461-113">**IDataObject：：：：的**</span><span class="sxs-lookup"><span data-stu-id="6e461-113">**IDataObject::GetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[<span data-ttu-id="6e461-114">**IDataObject：： SetData**</span><span class="sxs-lookup"><span data-stu-id="6e461-114">**IDataObject::SetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




