---
description: 安裝例外狀況套件。
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: InstallComponentW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990712"
---
# <a name="installcomponentw-function"></a>InstallComponentW 函式

安裝例外狀況套件。

## <a name="syntax"></a>語法


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*InfPath* \[在\]
</dt> <dd>

要處理之例外狀況 INF 的路徑。

</dd> <dt>

*CompGuid* \[在中，選擇性\]
</dt> <dd>

要安裝之例外狀況元件的 GUID。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

用來控制安裝行為的旗標。 這個參數可以是下列值的組合。



| 值                                                                                                                                                                                                                                                               | 意義                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**COMP \_旗標 \_ 強制**</dt> <dt>0x00000020</dt> </dl>                             | 略過檔案取代的版本檢查。<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**COMP \_旗標 \_ 需要 \_ 卸載**</dt><dt></dt> </dl>        | 備份檔案，以供卸載元件時使用。<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**COMP \_旗標 \_ 無 \_ 覆寫**</dt><dt></dt> </dl>                 | 如果例外狀況元件版本與已安裝的元件相同，則略過備份檔案。 此旗標用於重新安裝案例中。<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_旗標 \_ NOUI**</dt> <dt>0x00000002</dt> </dl>                                | 隱藏所有 UI。<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_旗標 \_ 更新 \_ DLLCACHE**</dt><dt></dt> </dl>        | 當更新系統檔案時，強制更新 DLLCACHE 目錄。<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**COMP \_旗 \_ 標 \_ 使用 \_ SVCPACK**</dt>快取 <dt></dt> </dl> | 使用 Windows service pack 安裝所快取的檔案來取代備份的檔案。<br/>                                                                |



 

</dd> <dt>

*>vermajor* \[在中，選擇性\]
</dt> <dd>

例外狀況元件的主要版本。

</dd> <dt>

*>verminor* \[在中，選擇性\]
</dt> <dd>

例外狀況元件的次要版本。

</dd> <dt>

*VerBuild* \[在中，選擇性\]
</dt> <dd>

例外狀況元件的組建版本。

</dd> <dt>

*VerQFE* \[在中，選擇性\]
</dt> <dd>

例外狀況元件的修正程式修訂。

</dd> <dt>

*名稱* \[在中，選擇性\]
</dt> <dd>

如果作業系統偵測到 Windows 檔案保護保護檔案已損毀、遭篡改或損毀，Windows 檔案保護對話方塊所顯示之元件的描述性字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式會傳回 **HRESULT** 值， (S \_ OK 或失敗碼) 。 您可以針對0x20000100 值檢查失敗碼，以判斷失敗是否因為需要重新開機。

## <a name="remarks"></a>備註

例外狀況套件是 Windows 系統檔案，這些檔案是在完整套件 Windows 版本之外發行，而且會更新作業系統檔案。 例外狀況套件只是由已獲得授權更新 Windows 系統檔案的作業系統小組所撰寫。

若要安裝和卸載未受 Windows 檔案保護保護的檔案，請使用 [一般安裝](https://msdn.microsoft.com/library/ms794585.aspx)函式中記載的功能。 若要安裝設備磁碟機，venders 應該使用 [裝置安裝功能](https://msdn.microsoft.com/library/ms792954.aspx) 和 [PnP 設定管理員](https://msdn.microsoft.com/library/ms790838.aspx)函式中記載的功能。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 
