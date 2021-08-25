---
description: GetNPPBlobTable 函式會抓取代表本機電腦上註冊 Nic 的 NPP BLOB 資料表。
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: 'GetNPPBlobTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 49920df1be929eb9b35781aeabdcdf47167e82a94066e2d3237207dd00b08f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910698"
---
# <a name="getnppblobtable-function"></a>GetNPPBlobTable 函式

**GetNPPBlobTable** 函式會抓取代表本機電腦上註冊 NIC 的 NPP BLOB 資料表。

## <a name="syntax"></a>語法


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFilterBlob* \[在\]
</dt> <dd>

篩選 BLOB 的控制碼，限制在資料表中傳回的 NPP Blob。

</dd> <dt>

*ppBlobTable* \[擴展\]
</dt> <dd>

[Blob \_ 資料表](blob-table.md)結構的指標，其中包含至少一個 blob 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                                | 描述                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ NPP \_ DLL**</dt> </dl>         | 在 NPP 目錄中找不到任何 Dll。<br/>                    |
| <dl> <dt>**NMERR \_ 沒有 \_ 有效的 \_ NPP \_ DLL**</dt> </dl> | NPP 目錄中的 Dll 都不是有效的 NPP Dll。<br/>  |
| <dl> <dt>**NMERR \_ 沒有 \_ 相符的 \_ NPPS**</dt> </dl>   | 探索到 NPP Blob，但未通過篩選測試。<br/> |
| <dl> <dt>**NMERR \_ OUT \_ OF \_ 記憶體**</dt> </dl>       | 網路監視器無法配置記憶體。<br/>            |



 

## <a name="remarks"></a>備註

*HFilterBlob* 命名的 blob 也可以是特殊的 blob。

如果您將篩選 BLOB 中的旗標設定為 **TRUE**，則傳回的 blob 資料表也可以包含特殊 blob。

如果以 *hFilterBlob* 命名的 blob 是特殊 blob，網路監視器 UI 將會嘗試處理它。 例如，假設先前的呼叫會從遠端 NPP 傳回特殊的 BLOB。 應用程式會插入必要的標記、電腦 \_ 名稱。 然後，搜尋工具會將此 BLOB 傳遞到遠端 NPP，然後傳回與電腦名稱稱相關聯的 NPP Blob 資料表。

為了終結所有傳回的 Blob 和 BLOB 資料表，呼叫端會負責呼叫 **DestroyBlob** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




