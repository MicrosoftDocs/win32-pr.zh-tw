---
description: DoConfigure 方法必須由監視器所執行。 MCSVC 會呼叫這個方法來取得 capture 的設定資訊。
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: 'IMonitor： (Netmon 的:D oConfigure 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112800"
---
# <a name="imonitordoconfigure-method"></a>IMonitor：:D oConfigure 方法

**DoConfigure** 方法必須由監視器所執行。 MCSVC 會呼叫這個方法來取得 capture 的設定資訊。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

監視器實例的名稱。

</dd> <dt>

*pConfiguration* \[在\]
</dt> <dd>

MCSVC 所提供的設定字串。 此監視器必須剖析此字串中的設定資料。

</dd> <dt>

*ppScriptInstance* \[擴展\]
</dt> <dd>

用來設定監視的 HTML 字串位址。 如果預設腳本用於設定，則此值應該設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同，而且 MCSVC 將會執行監視器。

如果此方法不成功，則傳回值會是錯誤碼。 NMERR 監視器設定的 \_ 傳回值 \_ \_ 是可接受的，但是當傳回此錯誤時，在未來的 **DoConfigure** 呼叫成功之前，無法啟動監視器。 任何其他錯誤都會導致無法啟用監視的實例。

## <a name="remarks"></a>備註

MCSVC 會在連接到網路之後，以及呼叫 [IRTC：： Configure](irtc-configure.md) 方法之前呼叫這個方法。

此監視器可以儲存此呼叫所提供的資訊、更新 HTML 腳本或設定字串，以及在 NPP BLOB 中設定 [捕捉篩選](capture-filters.md) 。

MCSVC 可能會呼叫這個方法數次，但在監視器正在捕獲資料時無法呼叫。 請注意，每次 [NPP](network-packet-providers.md) 啟動捕獲時，都必須設定網路的連接。 這項限制包含 NPP 啟動和停止相同捕捉的情況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




