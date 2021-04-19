---
description: AMOVIESETUP \_ 篩選結構包含註冊篩選的資訊。
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: 'AMOVIESETUP_FILTER 結構 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980175"
---
# <a name="amoviesetup_filter-structure"></a>AMOVIESETUP \_ 篩選結構

**AMOVIESETUP \_ 篩選** 結構包含註冊篩選的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a>成員

<dl> <dt>

**Clsid**
</dt> <dd>

篩選準則的類別識別碼。

</dd> <dt>

**strName**
</dt> <dd>

篩選的名稱。

</dd> <dt>

**dwMerit**
</dt> <dd>

篩選業績。 在建立篩選圖形時，由 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面使用。 如需相關值的清單，請參閱「 [業績](merit.md)」。

</dd> <dt>

**nPins**
</dt> <dd>

*LpPin* 陣列中的元素數目。 如果 *lpPin* 為 **Null**，請將此成員設定為零。

</dd> <dt>

**lpPin**
</dt> <dd>

[**AMOVIESETUP \_ 釘**](amoviesetup-pin.md)選結構陣列的指標，大小為 *nPins*。 這個陣列的每個成員都描述篩選上的釘選。

</dd> </dl>

## <a name="remarks"></a>備註

如需使用此結構的詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。 此結構僅適用于在預設篩選準則分類 (CLSID LegacyAmFilterCategory) 中註冊的篩選準則 \_ 。 若要在不同類別中註冊篩選準則，請使用 [**IFilterMapper2：： RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) 方法，如實 [DllRegisterServer](implementing-dllregisterserver.md)中所述。

> [!Note]  
> Combase 標頭檔隨附于 [DirectShow 基類](directshow-base-classes.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Combase (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 結構](directshow-structures.md)
</dt> </dl>

 

 




