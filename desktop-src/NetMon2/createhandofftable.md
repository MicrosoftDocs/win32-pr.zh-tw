---
description: CreateHandoffTable 函式會建立一個包含在剖析器 INI 檔案中儲存之遞交集資訊的遞交資料表。
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: 'CreateHandoffTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70709223d5dcebcae819389feb8623006b793126a911fc674491b1d665268056
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911198"
---
# <a name="createhandofftable-function"></a>CreateHandoffTable 函式

**CreateHandoffTable** 函式會建立一個包含在剖析器 INI 檔案中儲存之遞交集資訊的 [*遞交資料表*](h.md)。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*secName* \[在\]
</dt> <dd>

字串，表示要在其中放置遞交集資訊的 INI 檔區段。

</dd> <dt>

*iniFile* \[在\]
</dt> <dd>

包含剖析器 INI 檔案名的字串。

</dd> <dt>

*hTable* \[擴展\]
</dt> <dd>

網路監視器所建立和維護的 **HANDOFFTABLE** 結構的控制碼。

</dd> <dt>

*nMaxProtocolEntries* \[在\]
</dt> <dd>

指定交付資料表可處理的專案數上限的數位。

</dd> <dt>

*基底* \[在\]
</dt> <dd>

儲存在 INI 檔案中的交付集數位的數位基底。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是提交資料表中的專案數。

如果函式不成功，則傳回值為零。

## <a name="remarks"></a>備註

網路監視器所建立的交付資料表是以剖析器 INI 中提供的資訊為基礎。 然後，您可以使用提交資料表的傳回控制碼，來取得包含在資料表中其中一個通訊協定的控制碼。 若要取得其中一個通訊協定的控制碼，請呼叫 [GetProtocolFromTable](getprotocolfromtable.md)。

請注意，剖析器應用程式永遠不會直接存取 **HANDOFFTABLE** 結構。 此結構是由網路監視器建立和維護。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




