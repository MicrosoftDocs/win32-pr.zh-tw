---
description: 載入監視 DLL。
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: 'OnLoadingDLL 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6049684798d6dda9030abd667c28a62f4b19f9b4e66a831ef4c1d2caa880fb1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676868"
---
# <a name="onloadingdll-function"></a>OnLoadingDLL 函式

**OnLoadingDLL** 函式會載入監視器 DLL。

## <a name="syntax"></a>語法


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFilterBlob* \[in、out\]
</dt> <dd>

MCSVC 用來比對具有可用 Nic 之監視的 BLOB。 此參數一律包含 [IRTC](irtc.md) 介面的要求，因此大部分的監視器都不需要將任何專案新增至 BLOB。 不過，自訂監視可以新增額外的篩選準則 (例如，MAC 類型必須是乙太網路) 。

</dd> <dt>

*pCreateFlags* \[在\]
</dt> <dd>

旗標，指出 MCSVC 如何控制監視的建立。 此參數必須是下列其中一個值：



| 值                                                                                                                                                                                                            | 意義                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ 為 \_ \_ 每個 \_ 網卡建立一個**</dt> </dl>          | MCSVC 可確保每個 NIC 都只會有一個此監視實例存在。 只有當第一個實例被終結時，才能建立第二個實例。<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**MCS \_ 預設會建立 \_ \_ \_ 設置**</dt> </dl> | 如果監視器具有預設內部設定，則在建立實例之前，MCSVC 不需要使用者設定監視。<br/>  |



 

</dd> <dt>

*ppDefaultName* \[擴展\]
</dt> <dd>

指標，指向監視的預設名稱的位址。 建立監視的實例時，MCSVC 會使用預設名稱。

例如，如果傳回的預設名稱是「路由器監視器」，第一個監視實例會是「路由器監視器1」，第二個則是「RouterMonitor2」，依此類推。 如果傳回 **Null** ，則 MCSVC 會使用 DLL 的名稱。

</dd> <dt>

*ppDescription* \[擴展\]
</dt> <dd>

指向監視之描述位址的指標。 描述會傳遞至監視器控制工具，此工具會使用描述向使用者指出監視器是否存在。 這個參數可以傳回 **Null**。

</dd> <dt>

*ppDefaultScript* \[擴展\]
</dt> <dd>

指標，指向用來設定監視之預設 HTML 表單腳本的位址。 雖然監視的實例可以改變自己的腳本，但大部分的監視器只會從檔案載入腳本一次。 *PpDefaultScript* 的值可以是 **Null**;不過，您無法從外部設定監視，也可以稍後再提供腳本。 在這裡提供預設腳本會更有效率。

</dd> <dt>

*ppDefaultConfig* \[擴展\]
</dt> <dd>

建立時用於設定監視之預設字串的位址。 這個參數可以設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 S \_ OK; 這與 >aad-userreadusingalternativesecurityid-noerror 相同。

如果函式不成功，MCSVC 會從其所有清單中省略指定的監視器;之後，就無法建立此類型的監視。

## <a name="remarks"></a>備註

**OnLoadingDLL** 函式會在第一次載入 DLL 時，由 MCSVC 呼叫一次。 然後，DLL 會提供預設值，在建立監視的實例時，MCSVC 會使用此值。

監視器必須配置傳回給 MCSVC 的字串所需的所有記憶體。 傳回時，MCSVC 會建立所有字串的複本，且不會嘗試釋放傳回的字串。

監視器應使用 BLOB 協助程式函數來改變篩選 BLOB。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




