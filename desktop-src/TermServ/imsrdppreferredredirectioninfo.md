---
title: IMsRdpPreferredRedirectionInfo 介面
description: 提供屬性，以使用重新導向伺服器來控制。
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- IMsRdpPreferredRedirectionInfo 介面遠端桌面服務
- IMsRdpPreferredRedirectionInfo 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464576"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a>IMsRdpPreferredRedirectionInfo 介面

提供屬性，以使用重新導向伺服器來控制。

## <a name="members"></a>成員

**IMsRdpPreferredRedirectionInfo** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMsRdpPreferredRedirectionInfo** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpPreferredRedirectionInfo** 介面具有這些屬性。



| 屬性                                                                                               | 存取類型           | Description                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**UseRedirectionServerName**](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | 讀取/寫入<br/> | 取得和設定是否使用重新導向伺服器名稱。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpPreferredRedirectionInfo 定義為 FDD029F9-9574-4DEF-8529-64B521CCCAA4<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

