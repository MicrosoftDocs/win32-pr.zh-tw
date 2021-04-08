---
title: 'MrmCreateResourceFile 函式 (MrmResourceIndexer) '
description: 在指定的資料夾中，于磁片上建立一個名為 \ 0034; resources. pri \ 0034; ) 或檔案的 (PRI 檔案。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- MrmCreateResourceFile 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686298"
---
# <a name="mrmcreateresourcefile-function"></a>MrmCreateResourceFile 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

在指定的資料夾中，于磁片上建立名稱為 "resources. pri" ) 或檔案的 PRI 檔案 (。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引子* \[在\]
</dt> <dd>

類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

識別資源索引子的控制碼，以從中建立 PRI 檔案。

</dd> <dt>

*packagingMode* \[在\]
</dt> <dd>

類型： **[ **MrmPackagingMode**](mrmpackagingmode.md)**

指定 PRI 檔案是否應獨立、依資源限定詞自動分割，或為資源套件。

</dd> <dt>

*packagingOptions* \[在\]
</dt> <dd>

類型： **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

指定 PRI 檔案的其他選項。

</dd> <dt>

*outputDirectory* 
</dt> <dd>

類型： **PCWSTR**

要在其中儲存 PRI 檔案的資料夾路徑。

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

 

