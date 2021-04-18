---
title: 'MrmFreeMemory 函式 (MrmResourceIndexer) '
description: 釋放 MrmCreateConfigInMemory、MrmCreateResourceFileInMemory、MrmDumpPriFileInMemory 和 MrmDumpPriDataInMemory 所配置的記憶體。
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- MrmFreeMemory 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965109"
---
# <a name="mrmfreememory-function"></a>MrmFreeMemory 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

釋放 [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md)、 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)、 [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)和 [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)所配置的記憶體。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*資料* \[在\]
</dt> <dd>

類型： **BYTE \** _

由 [_ *MrmCreateConfigInMemory* *](mrmcreateconfiginmemory.md)、 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)、 [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)或 [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)所配置和傳回之記憶體的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1803版桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | \[僅限 Windows Server desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>MrmResourceIndexer。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Mrmsupport .lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[套件資源索引 (PRI) API 和自訂建置系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

