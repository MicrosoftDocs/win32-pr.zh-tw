---
description: Merge 物件的連線方法會將模組連接到其他功能。 模組必須已經合併到資料庫中，或合併到資料庫中。 在呼叫此函式之前，此功能必須存在。
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: '合併。連線方法 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c28aafaac9f8224ea4f622b2e63f81d9dc458d72e98c6e22c348087794e9e7a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926668"
---
# <a name="mergeconnect-method"></a>合併。連線方法

[**Merge**](merge-object.md)物件的 **連線** 方法會將模組連接到其他功能。 模組必須已經合併到資料庫中，或合併到資料庫中。 在呼叫此函式之前，此功能必須存在。

除非呼叫 [**CloseDatabase**](merge-closedatabase.md) 方法，並將 *BCommit* 設定為 **TRUE**，否則對資料庫所做的變更不會儲存至磁片。

## <a name="syntax"></a>語法


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*功能* 
</dt> <dd>

存在於資料庫中的功能名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

錯誤可能會透過 [ [**錯誤**](merge-errors.md) ] 屬性來抓取。 錯誤和參考用訊息會張貼至目前的記錄檔。

### <a name="c"></a>C++

請參閱 [**連線**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect)函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
