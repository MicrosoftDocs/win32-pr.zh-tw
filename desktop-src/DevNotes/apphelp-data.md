---
description: 包含 Apphelp 資料資訊。
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: APPHELP_DATA 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972325"
---
# <a name="apphelp_data-structure"></a>APPHELP \_ 資料結構

包含 Apphelp 資料資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**dwFlags**
</dt> <dd>

這個參數可以是下列其中一個值。

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_停用 \_ 填充碼** (0x00000001) 
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_停用 \_ APPHELP** (0x00000002) 
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_APPHELP \_ NOUI** (0x00000004) 
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_APPHELP \_ 取消** (0x10000000) 
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_停用 \_ SXS** (0x00000010) 
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_停用 \_ LAYER** (0x00000020) 
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_停用 \_ 驅動程式** (0x00000040) 
</dt> </dl> </dd> <dt>

**dwSeverity**
</dt> <dd>

此參數可以 APPTYPE \_ 無 (0) 。

</dd> <dt>

**dwHTMLHelpID**
</dt> <dd>

HTML 說明識別碼。

</dd> <dt>

**szAppName**
</dt> <dd>

應用程式名稱。

</dd> <dt>

**trExe**
</dt> <dd>

對應之可執行檔的 [**TAGREF**](tagref.md) 。

</dd> <dt>

**szURL**
</dt> <dd>

Apphelp online 連結的 URL。

</dd> <dt>

**szLink**
</dt> <dd>

**SzURL** 的連結文字。

</dd> <dt>

**szAppTitle**
</dt> <dd>

Apphelp 訊息的標題。

</dd> <dt>

**szContact**
</dt> <dd>

廠商連絡人資訊。

</dd> <dt>

**szDetails**
</dt> <dd>

詳細的 Apphelp 訊息。

</dd> <dt>

**dwData**
</dt> <dd>

應用程式所管理的使用者定義資料。

</dd> <dt>

**bSPEntry**
</dt> <dd>

如果這個專案是在 service pack 資料庫中，則這個成員為 **TRUE** ，否則為 **FALSE** 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




