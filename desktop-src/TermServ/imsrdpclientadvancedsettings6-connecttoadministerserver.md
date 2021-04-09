---
title: IMsRdpClientAdvancedSettings6 ConnectToAdministerServer 屬性
description: 取得或指定 ActiveX 控制項是否應該基於系統管理目的嘗試連接至伺服器。
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- ConnectToAdministerServer 屬性遠端桌面服務
- ConnectToAdministerServer 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ConnectToAdministerServer 屬性
- ConnectToAdministerServer 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ConnectToAdministerServer 屬性
- ConnectToAdministerServer 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ConnectToAdministerServer 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025102"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a>IMsRdpClientAdvancedSettings6：： ConnectToAdministerServer 屬性

取得或指定 ActiveX 控制項是否應該基於系統管理目的嘗試連接至伺服器。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a>屬性值

**變異 \_TRUE** 表示讓 ActiveX 控制項基於系統管理目的嘗試連接到伺服器;否則 **\_ 為 VARIANT FALSE**。 預設值為 **VARIANT \_ FALSE**。

## <a name="remarks"></a>備註

若要使用 **ConnectToAdministerServer**，您必須執行遠端桌面連線 (RDC) 用戶端6.1 版或更新版本。

> [!Note]  
> RDC 6.1 版 (6.0.6001) 支援遠端桌面通訊協定6.1。 RDC 6.1 隨附于 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 。

 

**ConnectToAdministerServer** 會將您連線至遠端伺服器上用於系統管理目的的會話。 如果遠端桌面工作階段主機 (RD 工作階段主機) 角色服務安裝在遠端伺服器上， **ConnectToAdministerServer** 會執行下列動作：

-   停用會話的遠端桌面服務用戶端存取授權。
-   停用會話的時區重新導向。
-   停用會話的遠端桌面連線代理人 (RD 連線代理人) 重新導向。
-   停用會話的隨插即用裝置重新導向。
-   將會話的遠端會話主題變更為 Windows 傳統。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





