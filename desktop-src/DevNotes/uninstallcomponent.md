---
description: 移除例外狀況套件。
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: UninstallComponent 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: d6b4ce8e447bc884d1b3ee64505d230b2e069ce6cda1630b027b8a48da68beda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001108"
---
# <a name="uninstallcomponent-function"></a>UninstallComponent 函式

移除例外狀況套件。

## <a name="syntax"></a>語法


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CompGuid* \[在中，選擇性\]
</dt> <dd>

要卸載之例外狀況元件的 GUID。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

用來控制安裝行為的旗標。 這個參數可以是下列值的組合。



| 值                                                                                                                                                                                                         | 意義                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ 旗標 \_ NOUI**</dt> </dl>                                          | 隱藏所有 UI。<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_ 旗標 \_ 更新 \_ DLLCACHE**</dt> </dl>        | 當更新系統檔案時，強制更新 DLLCACHE 目錄。<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**使用 SVCPACK 快取的複合 \_ 旗標 \_ \_ \_**</dt> </dl> | 使用 Windows service pack 安裝快取的檔案來取代備份的檔案。<br/> |



 

</dd> <dt>

*>Vermajor* \[在中，選擇性\]
</dt> <dd>

要卸載之例外狀況元件的主要版本。

</dd> <dt>

*>Verminor* \[在中，選擇性\]
</dt> <dd>

要卸載之例外狀況元件的次要版本。

</dd> <dt>

*VerBuild* \[在中，選擇性\]
</dt> <dd>

要卸載之例外狀況元件的組建版本。

</dd> <dt>

*VerQFE* \[在中，選擇性\]
</dt> <dd>

要卸載之例外狀況元件的修正程式修訂。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

例外狀況套件是在完整封裝之外發行的 Windows 系統檔案 Windows 版本和更新作業系統檔案。 例外狀況套件只是由已獲得授權更新 Windows 系統檔案的作業系統小組所撰寫。

若要安裝和卸載未受 Windows 檔案保護保護的檔案，請使用[一般安裝](https://msdn.microsoft.com/library/ms794585.aspx)函式中記載的功能。 若要安裝設備磁碟機，venders 應該使用 [裝置安裝功能](https://msdn.microsoft.com/library/ms792954.aspx) 和 [PnP 設定管理員](https://msdn.microsoft.com/library/ms790838.aspx)函式中記載的功能。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 
