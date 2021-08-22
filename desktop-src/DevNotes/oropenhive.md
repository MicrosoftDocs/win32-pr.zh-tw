---
description: 將指定的登錄 hive 檔案載入記憶體中，並驗證 hive。
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: 'OROpenHive 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 86ff3d6ff15b030054d40ca7131e521cedb59ebf20c4942951f0e141f27a2840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076012"
---
# <a name="oropenhive-function"></a>OROpenHive 函式

將指定的登錄 hive 檔案載入記憶體中，並驗證 hive。

## <a name="syntax"></a>語法


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpHivePath* \[在\]
</dt> <dd>

Unicode 字串的指標，指定要載入記憶體中的登錄 hive 檔案的名稱。 這可以是使用 [**ORSaveHive**](orsavehive.md) 函式所儲存或使用 [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) 或 [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) 函數所建立的 hive 檔案。 檔案大小必須小於 4 GB，且呼叫端必須具有檔案 \_ 的檔案讀取 \_ 資料存取權。 如需詳細資訊，請參閱檔案 [安全性和存取權限](../fileio/file-security-and-access-rights.md)。

</dd> <dt>

*phkResult* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收已載入之離線登錄 hive 的根目錄控制碼。 如果無法開啟登錄 hive 檔案或驗證失敗，函式會將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。 可能的錯誤代碼包括下列各項：

-   如果檔案大小為空白或大於 4 GB，則函式會傳回錯誤 \_ BADDB。
-   如果呼叫端沒有開啟檔案的必要存取權限，則函式會傳回 \_ 拒絕存取錯誤 \_ 。
-   如果登錄 hive 驗證失敗，此函式會傳回錯誤，而不是登錄檔 \_ \_ \_ 。

## <a name="remarks"></a>備註

**OROpenHive** 函式是唯一可驗證登錄 hive 的離線登錄函式。 如果驗證失敗，則不會嘗試修復 hive。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows離線登錄庫1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
