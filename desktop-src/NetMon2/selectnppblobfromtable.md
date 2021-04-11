---
description: SelectNPPBlobFromTable 函式會從所提供的 NPP BLOB 資料表中選取一個 NIC。
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: 'SelectNPPBlobFromTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191502"
---
# <a name="selectnppblobfromtable-function"></a>SelectNPPBlobFromTable 函式

**SelectNPPBlobFromTable** 函式會從所提供的 NPP BLOB 資料表中選取一個 NIC。

## <a name="syntax"></a>語法


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

顯示 [ **選取網路** ] 對話方塊之視窗的控制碼。

</dd> <dt>

*pBlobTable* \[在\]
</dt> <dd>

提供的 BLOB 資料表指標。 網路監視器使用此資料表來填入 [ **選取網路** ] 對話方塊。

</dd> <dt>

*hBlob* \[擴展\]
</dt> <dd>

代表所選 NIC 之 BLOB 的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功且使用者選取 NIC，則傳回值為 NMERR \_ SUCCESS; *hBlob* 所指向的 BLOB 會填入。

如果使用者未選取 NIC，則傳回值為 NMERR \_ NO \_ NPP \_ SELECTED。

如果函式不成功，則傳回值為另一個 NMERR 值。

## <a name="remarks"></a>備註

當呼叫時，網路監視器會顯示 [ **選取網路** ] 對話方塊，您可以使用此對話方塊來選取 NIC。 代表所選 NIC 的 NPP BLOB 會傳回到呼叫應用程式。

若要瞭解您可以選取 Nic 的各種方式，請參閱 [選取網路介面卡](selecting-a-network-interface-card.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[特殊 BLOB 專案](special-blob-entries.md)
</dt> </dl>

 

 




