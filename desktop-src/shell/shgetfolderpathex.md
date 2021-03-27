---
UID: ''
title: SHGetFolderPathEx 函式
description: 抓取 KNOWNFOLDERID 所識別之已知資料夾的路徑。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "104971660"
---
# <a name="shgetfolderpathex-function"></a>SHGetFolderPathEx 函式

## <a name="description"></a>Description

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。
Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

抓取資料夾的 [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)所識別之已知資料夾的完整路徑。
這可讓您設定字串緩衝區的初始大小，藉此擴充 [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 。

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a>參數

### <a name="rfid-in"></a>rfid [in]

識別資料夾之 **KNOWNFOLDERID** 的參考。

### <a name="dwflags-in"></a>dwFlags [in]

指定特殊抓取選項的旗標。
這個值可以是 0;否則，會有一或多個 [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) 值。

### <a name="htoken-in-optional"></a>hToken [in，optional]

代表特定使用者的 [存取權杖](/windows/desktop/SecAuthZ/access-tokens) 。
如果這個參數是 **Null**，這是最常見的使用方式，則函式會要求目前使用者的已知資料夾。

藉由傳遞該使用者的 *hToken* 來要求特定使用者的資料夾。
這通常是在具有足夠許可權的服務內容中完成，以取得指定使用者的權杖。
該權杖必須以 [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) 和 [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) 許可權開啟。
在某些情況下，您也必須包含 [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects)。
除了傳遞使用者的 *hToken* 之外，還必須裝載該特定使用者的登錄 hive。
如需存取控制問題的進一步討論，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control) 。

指派 *hToken* 參數-1 的值表示預設使用者。
這可讓 [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 的用戶端找到資料夾位置 (例如，預設使用者的 **桌面** 資料夾) 。
建立任何新的使用者帳戶時，預設的使用者使用者設定檔會重複，並包含 **檔** 和 **桌面** 等特殊資料夾。
任何新增至預設使用者資料夾的專案也會出現在任何新的使用者帳戶中。
請注意，存取預設使用者資料夾需要系統管理員許可權。

### <a name="pszpath-out"></a>pszPath [out]

以 null 結束的 Unicode 字串。
這個緩衝區的大小必須是 cchPath。
當 **SHGetFolderPathEx** 成功傳回時，此參數會包含已知資料夾的路徑。

### <a name="cchpath-in"></a>cchPath [in]

*PpszPath* 緩衝區的大小（以字元為單位）。

## <a name="returns"></a>傳回

如果成功，則傳回 **S_OK** ，否則傳回錯誤值。

## <a name="remarks"></a>備註

因為 [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 是 [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)的包裝函式，所以此函式 (**SHGetFolderPathEx**) 也可作為 **SHGetFolderPath** 的擴充功能。

## <a name="see-also"></a>另請參閱

[KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)

[KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[SHGetKnownFolderIDList](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
