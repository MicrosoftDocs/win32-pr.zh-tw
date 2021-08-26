---
description: SetStreamNumber 方法會指定要從與此來源物件相關聯的來源檔案中讀取的資料流程。
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'IAMTimelineSrc：： SetStreamNumber 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae313121831dc2855a2f07ba3c7727e87736b77a8c5f98078d2237bb9520cf6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982958"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>IAMTimelineSrc：： SetStreamNumber 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`SetStreamNumber`方法會指定要從與此來源物件相關聯之來源檔案讀取的資料流程。

## <a name="syntax"></a>語法


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Val* 
</dt> <dd>

資料流程號碼，從與父群組之媒體類型相符的資料流程集合中。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

*Val* 參數會從一組符合父群組媒體類型的資料流程，而不是從原始程式檔中的整組資料流程指定資料流程號碼。 例如，假設檔案包含兩個影片串流和兩個音訊串流。 如果來源物件是在影片群組內，將 *Val* 設定為0會選取第一個影片串流。 呼叫端負責指定有效的資料流程號碼。

資料流程編號的預設值為零。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineSrc 介面**](iamtimelinesrc.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




