---
title: VirtualChannelGetInstance 進入點
description: 呼叫以讓外掛程式為 DLL 所執行的所有外掛程式建立 IWTSPlugin 介面的實例。
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- VirtualChannelGetInstance 進入點遠端桌面服務
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f96eac56f737d6f945c3d59d5cdf844e9cc65058a0460f620e6051830806ab99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868618"
---
# <a name="virtualchannelgetinstance-entry-point"></a>VirtualChannelGetInstance 進入點

呼叫以讓外掛程式為 DLL 所執行的所有外掛程式建立 [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) 介面的實例。

> [!Note]
>
> 這個函式是由外掛程式所執行，而且必須依名稱匯出，讓應用程式可以使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以動態方式連結至函數。
>
> 這個函式的原型不包含在任何公用標頭檔中，因此您必須如所示明確地宣告它。

 

## <a name="syntax"></a>語法


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*refiid* \[在\]
</dt> <dd>

指定要傳回的介面類別型。 這必須是 **IID \_ IWTSPlugin**。

</dd> <dt>

*pNumObjs* \[in、out\]
</dt> <dd>

會接收所抓取介面數目的 **ULONG** 變數位址。

</dd> <dt>

*ppObjArray* \[擴展\]
</dt> <dd>

接收介面指標之指標陣列的位址。 如果這個參數是 **Null**，則實值必須將 DLL 所執行的外掛程式數目放在 *pNumObjs* 參數中。 這可讓呼叫端為 *ppObjArray* 配置適當的大小陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個進入點成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



 

