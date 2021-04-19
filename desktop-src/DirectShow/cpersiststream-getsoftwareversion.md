---
description: 抓取此資料流程的軟體版本。
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: 'CPersistStream. GetSoftwareVersion 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994737"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a>CPersistStream. GetSoftwareVersion 方法

抓取此資料流程的軟體版本。

## <a name="syntax"></a>語法


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回包含版本號碼的 **DWORD** 。 每次變更資料流程的格式時，應該改變此函式，以傳回比之前更大的數位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 




