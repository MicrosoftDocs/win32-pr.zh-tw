---
description: CBaseAllocator 配置方法-配置方法會為緩衝區配置記憶體。
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: 'CBaseAllocator 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 975f373136759a0950e5052413eccb501176e7876531208fd20380ee7d1fb10a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966708"
---
# <a name="cbaseallocatoralloc-method"></a>CBaseAllocator 方法

`Alloc`方法會為緩衝區配置記憶體。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                       | Description                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>           | 緩衝區需求未變更。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 緩衝區需求已變更。<br/>     |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | 未設定緩衝區需求。<br/>     |



 

## <a name="remarks"></a>備註

[**CBaseAllocator：： Commit**](cbaseallocator-commit.md)方法會呼叫這個方法。

在基類中，此方法不會配置任何記憶體。 如果未設定緩衝區需求，則會傳回錯誤， \_ 如果需求沒有變更，則傳回 FALSE， \_ 如果需求已變更，則傳回 [確定]。

衍生類別應該覆寫這個方法，以執行實際的記憶體配置。 一般而言，衍生類別會執行下列步驟：

1.  呼叫基類執行，以判斷記憶體是否真的需要配置。
2.  配置記憶體。
3.  建立 [**CMediaSample**](cmediasample.md) 物件，其中包含步驟2中的記憶體區塊。
4.  將每個 **CMediaSample** 物件新增至免費範例清單， ([**CBaseAllocator：： m \_ lFree**](cbaseallocator-m-lfree.md)) 。

如需範例，請參閱 [**CMemAllocator：：分配**](cmemallocator-alloc.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




