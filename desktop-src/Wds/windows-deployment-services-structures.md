---
title: Windows部署服務結構
description: 下列結構會搭配 Windows 部署服務使用。
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4315ccd3d9540334b00f43fda6522e3eae28be2d038cfdd56fcd129e9e0aed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760248"
---
# <a name="windows-deployment-services-structures"></a>Windows部署服務結構

下列結構會搭配 Windows 部署服務使用。



| 結構                                                                         | 描述                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PXE \_ 位址**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | 指定封包的網路位址。                                                                        |
| [**PXE \_ DHCP \_ 訊息**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | 此結構會與 Windows 部署服務 PXE 伺服器 API 搭配使用。                                        |
| [**PXE \_ DHCP \_ 選項**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | 此結構會與 Windows 部署服務 PXE 伺服器 API 搭配使用。                                        |
| [**PXE \_ 提供者**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | 描述提供者。                                                                                              |
| [**WDS \_ CLI \_ 認證**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | 包含用來授權用戶端會話的認證。                                                           |
| [**WDS \_ TRANSPORTCLIENT \_ 要求**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | 由 [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) 函式使用。                     |
| [**TRANSPORTCLIENT \_ 會話 \_ 資訊**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | 由 [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) 回呼函數使用。 |
| [**WDS \_ TRANSPORTPROVIDER \_ INIT \_ 參數**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | 由 [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) 回呼函式使用。            |
| [**WDS \_ TRANSPORTPROVIDER \_ 設定**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | 由 [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) 回呼函式使用。            |



 

從 Windows 8 和 Windows Server 2012 開始提供下列各項。

| 結構                                          | 描述                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**PXE \_ DHCPV6 \_ 選項**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | 與 Windows 部署服務 PXE 伺服器 API 搭配使用。 |
| [**PXE \_ DHCPV6 \_ 訊息**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | DHCPV6 訊息。                                         |



 

 

 




