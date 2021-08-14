---
description: 針對 Windows 映像取得 (WIA) 2.0 裝置支援的傳輸格式建立枚舉器。
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'IWiaTransfer：： EnumWIA_FORMAT_INFO 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 5e497d389646249c03bfaa4ac8625ce2a440b97f4ff6b8c0b0942ec957d0901e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669473"
---
# <a name="iwiatransferenumwia_format_info-method"></a>IWiaTransfer：： EnumWIA \_ 格式 \_ 資訊方法

針對 Windows 映像取得 (WIA) 2.0 裝置支援的傳輸格式建立枚舉器。

## <a name="syntax"></a>語法


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppIEnum* \[擴展\]
</dt> <dd>

類型： **[ **IEnumWIA \_ 格式 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

列舉值的 [**IEnumWIA \_ 格式 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) 介面之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

應用程式必須在透過 *ppIEnum* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 
