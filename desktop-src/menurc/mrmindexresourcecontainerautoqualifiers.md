---
title: 'MrmIndexResourceContainerAutoQualifiers 函式 (MrmResourceIndexer) '
description: 為屬於 UWP 應用程式的 .resw/resources.resjson) 或 priinfo 或 prifile 資源 ( 檔內包含的字串資源編制索引。
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- MrmIndexResourceContainerAutoQualifiers 函式功能表與其他資源
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967561"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a>MrmIndexResourceContainerAutoQualifiers 函式

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

為屬於 UWP 應用程式的 .resw/resources.resjson) 或 priinfo 或 prifile 資源 ( 檔內包含的字串資源編制索引。 從 *containerPath* 參數推斷資源限定詞的清單。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。

## <a name="syntax"></a>語法


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引子* \[在\]
</dt> <dd>

類型： **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

識別將為字串資源編制索引之資源索引子的控制碼。

</dd> <dt>

*containerPath* \[在\]
</dt> <dd>

類型： **PCWSTR**

.Resw、. resources.resjson、. priinfo 或. prifile 的相對路徑，其中包含您想要編制索引的字串資源。 此路徑相對於您要產生 PRI 檔案之 UWP 應用程式的專案根目錄。 該專案根目錄是您傳遞至 [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)的 *projectRoot* 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式 \_ 成功，則為 [正常]，否則為其他值。 使用 winerror.h 中定義的成功 () 或失敗 ()  (宏) ，判斷成功或失敗。

## <a name="remarks"></a>備註

系統會從 *containerPath* 推斷資源限定詞。 例如，值為 L "en-us \\ \\ resources. .resw" 會新增具有限定詞 "language-en-us" 的字串資源。

當您稍後從此資源索引子產生 PRI 檔案時，資源檔的名稱將會用來做為這些資源的資源對應子樹名稱。

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

 

