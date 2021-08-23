---
description: 從屬於 EXE 專案的指定專案中抓取資料。
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 19477385fb70f65c560d1a13d479fc4c2ce1853220aff6ac32a75f3634a40d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815378"
---
# <a name="sdbquerydataextagid-function"></a>SdbQueryDataExTagID 函式

從屬於 EXE 專案的指定專案中抓取資料。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[在\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> <dt>

*tiExe* \[在\]
</dt> <dd>

EXE 專案的 [**TAGID**](tagid.md) 。

</dd> <dt>

*lpszDataName* \[在中，選擇性\]
</dt> <dd>

要抓取的資料輸入名稱。 若要指定多個專案，請以反斜線字元分隔名稱 ( " \\ " ) 。 如果此參數為 **Null**，則函式會嘗試傳回所有資料項目。

</dd> <dt>

*lpdwDataType* \[out、optional\]
</dt> <dd>

傳回之專案的資料類型。 這個參數可以是下列其中一個值：

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**REG \_ 二進位檔**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**REG \_ DWORD**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ 多重 \_ SZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ 無**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**REG \_ QWORD**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**REG \_ SZ**
</dt> </dl> </dd> <dt>

*lpBuffer* \[擴展\]
</dt> <dd>

接收資料的緩衝區。 如果緩衝區不夠大，無法包含資料，則函數會失敗，並傳回 **錯誤 \_ 的 \_ 緩衝區**。

</dd> <dt>

*lpcbBufferSize* \[in、out、optional\]
</dt> <dd>

*LpBuffer* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*ptiData* \[擴展\]
</dt> <dd>

資料輸入的 [**TAGID**](tagid.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回下列其中一個值。



| 傳回碼                                                                                                    | 描述                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>       | 一或多個輸入參數不正確。<br/>                  |
| <dl> <dt>**\_內部 \_ 資料庫 \_ 損毀錯誤**</dt> </dl> | 找不到 EXE 專案的資料項目目。<br/>               |
| <dl> <dt>**\_緩衝區不足的錯誤 \_**</dt> </dl>     | 緩衝區不夠大，無法包含資料項目目。<br/> |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl>      | 記憶體配置失敗。<br/>                               |
| <dl> <dt>**\_找不 \_ 到錯誤**</dt> </dl>               | 找不到名稱為 *lpszDataName* 的資料輸入。<br/>    |
| <dl> <dt>**錯誤 \_ 成功**</dt> </dl>                  | 函數已順利完成。<br/>                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




