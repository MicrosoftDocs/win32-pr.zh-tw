---
description: 深入瞭解： JET_ERR
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106974901"
---
# <a name="jet_err"></a>JET_ERR


_**適用于：** Windows |Windows Server_

## <a name="jet_err"></a>JET_ERR

**JET_ERR** 資料類型包含可延伸的 [儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)。

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>資料類型

JET_ERR

 (對應至 JET_errSuccess 的零值) 表示呼叫成功。 正值會針對在其他成功呼叫期間發生的非嚴重狀況發出警告。 負數值表示呼叫失敗。

### <a name="remarks"></a>備註

如需以 Hresult 傳回錯誤的相關資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md)。 如需有關設定資料庫以處理錯誤之旗標的詳細資訊，請參閱 [錯誤處理參數](./error-handling-parameters.md)。

### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md)  
[可擴充儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)  
[錯誤處理參數](./error-handling-parameters.md)
