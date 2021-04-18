---
title: 'IDeliveryOptimizationJob AddFileWithRanges 方法 (>deliveryoptimization .h) '
description: 將檔案新增至下載作業，並指定您想要下載的檔案範圍。
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- AddFileWithRanges 方法
- AddFileWithRanges 方法，IDeliveryOptimizationJob 介面
- IDeliveryOptimizationJob 介面，AddFileWithRanges 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965329"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>IDeliveryOptimizationJob：： AddFileWithRanges 方法

將檔案新增至下載作業，並指定您想要下載的檔案範圍。

## <a name="syntax"></a>語法


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fileId* \[在\]
</dt> <dd>

以 Null 終止的字串，表示已發佈內容的唯一識別碼。 針對未發佈的內容，這可以是任何唯一的字串，呼叫者可以用來識別作業內的檔案。

</dd> <dt>

*remoteUrl* \[在\]
</dt> <dd>

以 Null 終止的字串，其中包含伺服器上的檔案名。

</dd> <dt>

*localName* \[在\]
</dt> <dd>

以 Null 終止的字串，其中包含用戶端上的檔案名。

</dd> <dt>

*rangeCount* \[在中，選擇性\]
</dt> <dd>

*範圍* 中的元素數目。

</dd> <dt>

*範圍* \[在中，選擇性\]
</dt> <dd>

一或多個 [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) 結構的陣列，指定要下載的範圍。 請勿指定重複或重迭的範圍。

</dd> <dt>

*fileSize* \[在中，選擇性\]
</dt> <dd>

檔案大小，以位元組為單位。 如果呼叫端應用程式不知道大小，請傳入 **DO_UNKNOWN_FILE_SIZE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列傳回值以及其他值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>傳回碼</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong><strong>S_OK</strong></strong></dt> </dl></td>
<td>成功。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>本機檔案名為 Null 或空字串。 <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>E_ACCESSDENIED</strong></dt> </dl></td>
<td>使用者沒有許可權可寫入至用戶端上指定的目錄。<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_RANGE</strong></dt> </dl></td>
<td>其中一個範圍無效。 例如，InitialOffset 會設定為 <strong>BG_LENGTH_TO_EOF</strong>。<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </dl></td>
<td>您無法指定重複或重迭的範圍。 <br/>
<blockquote>
[!Note]<br />
範圍是依值的位移（而不是長度）來排序。 如果輸入的範圍具有相同的位移，但順序相反，則會傳回此錯誤。 例如，如果以該順序輸入100.5 和100.0，您將無法將檔案新增至作業。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_STATE</strong></dt> </dl></td>
<td>無法 <strong>BG_JOB_STATE_CANCELLED</strong> 或 <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>作業的狀態。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob 定義為 EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

