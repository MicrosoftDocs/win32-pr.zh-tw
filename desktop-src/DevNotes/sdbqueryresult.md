---
description: 包含查詢填充碼資料庫以符合可執行檔的結果。
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: SDBQUERYRESULT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936190"
---
# <a name="sdbqueryresult-structure"></a>SDBQUERYRESULT 結構

包含查詢填充碼資料庫以符合可執行檔的結果。

## <a name="syntax"></a>語法


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a>成員

<dl> <dt>

**atrExes**
</dt> <dd>

相符可執行檔的 **TAGREF** 值。 請注意，「 **SDB \_ 最大 \_ exe** 」定義為16。

</dd> <dt>

**adwExeFlags**
</dt> <dd>

這個參數可以是下列一或多個值。

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

**atrLayers**
</dt> <dd>

相符層的 **TAGREF** 值。 請注意，[ **SDB \_ 最大 \_ 層** ] 定義為8。

</dd> <dt>

**dwLayerFlags**
</dt> <dd>

這個參數可以是下列一或多個值。

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

**trApphelp**
</dt> <dd>

對應可執行檔之 apphelp 訊息的 **TAGREF** 值。

</dd> <dt>

**dwExeCount**
</dt> <dd>

**AtrExes** 中的元素數目。

</dd> <dt>

**dwLayerCount**
</dt> <dd>

**AtrLayers** 中的元素數目。

</dd> <dt>

**guidID**
</dt> <dd>

最後一個可執行檔的 GUID。

</dd> <dt>

**dwFlags**
</dt> <dd>

這個參數可以是下列一或多個值。

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

**dwCustomSDBMap**
</dt> <dd>

自訂填充碼資料庫的對應。 如果 **rgGuidDB** 有效，則會設定對應的位。

</dd> <dt>

**rgGuidDB**
</dt> <dd>

填充碼資料庫的 Guid。 請注意，[ **SDB \_ MAX \_ SDBS** ] 定義為16。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> </dl>

 

 




