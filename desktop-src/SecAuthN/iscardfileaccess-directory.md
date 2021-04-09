---
description: 目錄方法會從目前的目錄抓取指定類型的檔案清單。
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: ISCardFileAccess：:D 目錄方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848756"
---
# <a name="iscardfileaccessdirectory-method"></a>ISCardFileAccess：:D 目錄方法

\[**目錄** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**目錄** 方法會從目前的目錄抓取指定類型的檔案清單。

## <a name="syntax"></a>語法


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型類型* \[在\]
</dt> <dd>

要列出的 [*智慧卡*](../secgloss/s-gly.md) 檔案類型。



| 值                                                                                                                                                                                      | 意義                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**SC \_ 類型 \_ 目錄**</dt> </dl>           | 僅列出目錄檔。<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**SC \_ 類型 \_ 檔案**</dt> </dl>                             | 僅列出基本檔案。<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC \_ TYPE \_ ALL \_ FILES**</dt> </dl>                | 列出目錄和基本檔案。<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**SC \_ 類型 \_ 目錄 \_ 檔案**</dt> </dl> | 目錄檔案。<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**SC \_ 型別 \_ 透明 \_ EF**</dt> </dl> | 透明的基本檔案。<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**SC \_ 類型 \_ 固定 \_ EF**</dt> </dl>                   | 線性固定基本檔案。<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**SC \_ 類型 \_ 迴圈 \_ EF**</dt> </dl>                | 迴圈基本檔案。<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**SC \_ 類型 \_ 變數 \_ EF**</dt> </dl>          | 線性變數基本檔案。<br/>          |



 

</dd> <dt>

*ppFileList* \[擴展\]
</dt> <dd>

Bstr 的陣列，代表符合檔 *類型* 中規範的檔案清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                   | Description                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業已順利完成。<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效的參數。<br/>                             |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 介面尚未執行此方法。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                                 |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 傳入 *ppFileList* 的錯誤指標。<br/>  |



 

## <a name="remarks"></a>備註

如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
