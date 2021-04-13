---
title: IMsTscAdvancedSettings >iconindex 屬性
description: 指定目前圖示檔中的圖示索引。
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- '>iconindex 屬性遠端桌面服務'
- '>iconindex 屬性遠端桌面服務，IMsTscAdvancedSettings 介面'
- IMsTscAdvancedSettings 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面'
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面'
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面'
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面'
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面'
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面'
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面'
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，>iconindex 屬性
- '>iconindex 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面'
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，>iconindex 屬性
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be56eab5dbe7f03155c6082e4e70fc4bd439253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508556"
---
# <a name="imstscadvancedsettingsiconindex-property"></a>IMsTscAdvancedSettings：： >iconindex 屬性

指定目前圖示檔中的圖示索引。

> [!Note]  
> ActiveX 控制項 (MsRdp) 不支援這個屬性。 標準用戶端 (MsTsc.exe) 中包含的 MsTscAx.dll 程式庫都支援此功能。

 

此屬性是唯寫的。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a>屬性值

圖示的索引。

## <a name="error-codes"></a>錯誤碼

傳回 **\_ FALSE**。

## <a name="remarks"></a>備註

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





