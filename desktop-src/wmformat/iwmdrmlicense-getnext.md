---
title: 'IWMDRMLicense GetNext 方法 (Wmdrmsdk .h) '
description: GetNext 方法會載入清單中下一個專案的相關資訊。
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- GetNext 方法 windows Media 格式
- GetNext 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetNext 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc0905bc695d1317cc7e4a6a1933292ad68afa8f3e3aadb9572e7a7185f4089c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847135"
---
# <a name="iwmdrmlicensegetnext-method"></a>IWMDRMLicense：： GetNext 方法

**GetNext** 方法會載入清單中下一個專案的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                | 描述                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt> </dl> | 需要更新的內容撤銷清單。<br/> |
| <dl> <dt>**\_沒有 \_ 其他 \_ 專案的錯誤**</dt> </dl>      | 清單中沒有其他項目了。<br/>          |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 此方法已成功。<br/>                         |



 

## <a name="remarks"></a>備註

[**IWMDRMLicense**](iwmdrmlicense.md)介面的方法會一次提供單一授權的相關資料。 基礎物件包含一或多個授權的清單。 當您呼叫這個方法時，介面會將其內部參考移至清單中的下一個授權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





