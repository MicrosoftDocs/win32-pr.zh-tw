---
title: IMsRdpClientNonScriptable4 RedirectionWarningType 屬性
description: 控制通知使用者重新導向之對話方塊的存在和外觀。
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- RedirectionWarningType 屬性遠端桌面服務
- RedirectionWarningType 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、RedirectionWarningType 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966126"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a>IMsRdpClientNonScriptable4：： RedirectionWarningType 屬性

控制通知使用者重新導向之對話方塊的存在和外觀。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a>屬性值

設定對話方塊的型別，此對話方塊會通知使用者重新導向。

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000) 


</dt> <dd>

對話方塊不是發行者特定的。

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001) 


</dt> <dd>

對話方塊適用于未簽署的檔案。

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002) 


</dt> <dd>

此對話方塊適用于未知的發行者。

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003) 


</dt> <dd>

對話方塊適用于使用者的檔案。

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004) 


</dt> <dd>

協力廠商認證的檔案會顯示此對話方塊。

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005) 


</dt> <dd>

對話方塊不會顯示，因為應用程式是由受信任的發行者所發行。

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005) 


</dt> <dd>

對話方塊不會顯示，因為應用程式是由受信任的發行者所發行。

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

值 **RedirectionWarningTypeDefault** 是這個屬性的預設值，對無法控制對話方塊。 此案例中的控制屬性是在 [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)中 [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





