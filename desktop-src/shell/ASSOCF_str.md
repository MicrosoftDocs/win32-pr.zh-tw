---
description: 提供 IQueryAssociations 介面方法的資訊。
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: ASSOCF 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d52de3ce181033358fc20ca3e4f8759b61f72ed
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786694"
---
# <a name="assocf-enumeration"></a>ASSOCF 列舉

提供 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 介面方法的資訊。

## <a name="syntax"></a>Syntax




| C++ | 
|-----|
| <pre><code>typedef enum  {   ASSOCF_NONE                  = 0x00000000,  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,  ASSOCF_INIT_BYEXENAME        = 0x00000002,  ASSOCF_OPEN_BYEXENAME        = 0x00000002,  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,  ASSOCF_NOUSERSETTINGS        = 0x00000010,  ASSOCF_NOTRUNCATE            = 0x00000020,  ASSOCF_VERIFY                = 0x00000040,  ASSOCF_REMAPRUNDLL           = 0x00000080,  ASSOCF_NOFIXUPS              = 0x00000100,  ASSOCF_IGNOREBASECLASS       = 0x00000200,  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,  ASSOCF_IS_PROTOCOL           = 0x00001000,  ASSOCF_INIT_FOR_FILE         = 0x00002000} ASSOCF;</code></pre> | 




## <a name="constants"></a>常數

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ 無** 

未設定下列任何選項。

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ INIT \_ NOREMAPCLSID** 

指示 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 介面方法不要將 CLSID 值對應至 ProgID 值。

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ INIT \_ BYEXENAME** 

識別 [**IQueryAssociations：： Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init)的 *pwszAssoc* 參數值，做為可執行檔名稱。 如果未設定此旗標，則會將根金鑰設定為與 **.exe** 索引鍵相關聯的 progid，而不是可執行檔的 progid。

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ 開啟 \_ BYEXENAME** 

與 **ASSOCF \_ INIT \_ BYEXENAME** 相同。

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ INIT \_ DEFAULTTOSTAR** 

指定當 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法在根機碼下找不到要求的值時，應該嘗試從子機碼取得可比較的值 **\*** 。

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ INIT \_ DEFAULTTOFOLDER** 

指定當 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法在根機碼下找不到要求的值時，應該嘗試從 **資料夾** 子機碼取得可比較的值。

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS** 

指定只搜尋 **HKEY \_ 類別 \_ 根目錄** ，且應忽略 HKEY 的 **\_ 目前 \_ 使用者** 。

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOTRUNCATE** 

指定不應該截斷傳回字串。 相反地，會傳回錯誤值和完整字串所需的大小。

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF \_ 確認** 

指示 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法驗證資料是否正確。 此設定可讓 **IQueryAssociations** 方法從使用者的硬碟讀取資料以進行驗證。 例如，他們可以針對儲存在 .exe 檔案中的檔案，檢查登錄中的易記名稱。 設定此旗標通常可減少方法的效率。

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL** 

指示 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法略過 Rundll.exe，並傳回其目標的相關資訊。 通常 **IQueryAssociations** 方法會傳回命令字串中第一個 .exe 或 .dll 的相關資訊。 如果命令使用 Rundll.exe，設定這個旗標會告知方法忽略 Rundll.exe 並傳回其目標的相關資訊。

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOFIXUPS** 

指示 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 方法不要修正登錄中的錯誤，例如函式的易記名稱不符合 .exe 檔案中找到的函式。

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS** 

指定應該忽略 BaseClass 值。

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ INIT \_ IGNOREUNKNOWN** 

**Windows 7 中引進**。 指定應忽略「未知」 ProgID;相反地，會失敗。

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF \_ INIT \_ FIXED \_ PROGID** 

**Windows 8 引進**。 指定提供的 ProgID 應使用系統預設值進行對應，而不是目前的使用者預設值。

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ 是 \_ 通訊協定** 

**Windows 8 引進**。 指定值為通訊協定，且應使用目前的使用者預設值進行對應。

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ INIT \_ FOR \_ FILE** 

**Windows 8.1 引進**。 指定 ProgID 與副檔名為基礎的關聯。 搭配使用 **ASSOCF \_ INIT \_ FIXED \_ PROGID**。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]               |
| 最低支援的伺服器 | Windows 2000 Server \[僅限傳統型應用程式\]                                 |
| 標頭                   |  Shlwapi。h  |



## <a name="see-also"></a>另請參閱

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. 著作權所有，並保留一切權利。
