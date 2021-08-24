---
description: 選取註冊 NIC。
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: 'GetNPPBlobFromUI 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d3b88c369145d53d32d23773072f878d9834110e705cd8ff623a3726cbb98b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743878"
---
# <a name="getnppblobfromui-function"></a>GetNPPBlobFromUI 函式

**GetNPPBlobFromUI** 函式會選取註冊 NIC。

## <a name="syntax"></a>語法


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

顯示 [ **選取網路** ] 對話方塊之視窗的控制碼。

</dd> <dt>

*hFilterBlob* \[在\]
</dt> <dd>

[*篩選 BLOB*](f.md)的控制碼，用來限制顯示的 nic。

</dd> <dt>

*phBlob* \[擴展\]
</dt> <dd>

BLOB 控制碼的指標，代表選取的 NIC。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (使用者選取 NIC) ，傳回值會 NMERR \_ 成功，而且 *phBlob* 指向的 BLOB 會填入。

如果使用者未選取 NIC，則傳回值為 **NMERR \_ NO \_ NPP \_ SELECTED**。

如果函式不成功，則傳回值為另一個 NMERR 值。

## <a name="remarks"></a>備註

當呼叫時，網路監視器會顯示 [ **選取網路** ] 對話方塊，您可以使用此對話方塊來選取 NIC。 代表 NIC 的 NPP BLOB 會傳回給呼叫的應用程式。

如果以 *hFilterBlob* 命名的 blob 是 [*特殊的 blob*](s.md)，則搜尋工具會嘗試處理它。 例如，先前從遠端 NPP 傳回特殊 BLOB 的呼叫。 應用程式已插入必要的標記、電腦 \_ 名稱。 在這種情況下，搜尋工具會將此 BLOB 傳遞到遠端 NPP，然後傳回 NPP Blob 的表格，代表所要求的電腦。 這些遠端 NPP Blob 將會出現在對話方塊中。

呼叫端必須呼叫 [DestroyBlob](destroyblob.md) 函式，此函式會在不再需要時終結傳回的 BLOB。



| 如需下列項目的詳細資訊 | 請參閱                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| 選取 Nic 的三種方式  | [選取網路介面卡](selecting-a-network-interface-card.md) |
| 指定篩選 BLOB   | [指定篩選 BLOB](specifying-a-filter-blob.md)                     |



 

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

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SelectNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 




