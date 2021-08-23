---
description: 以下是用來管理列印票證的函數。
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: 列印票證 API 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a908da3aee9e9fa1c3b7181261164860be95193cb4dc0d34a7fe17e6f2a4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033916"
---
# <a name="print-ticket-api-functions"></a>列印票證 API 函式

以下是用來管理列印票證的函數。

## <a name="in-this-section"></a>本節內容



| 函式                                                                                  | 描述                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | 將 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構轉換為列印票證。<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | 將列印票證轉換成 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構。<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | 合併兩個列印票證，並傳回有效的可用列印票證。<br/>                                                                          |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | 關閉列印票證提供者控制碼。<br/>                                                                                                      |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | 將 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構轉換成 [**IStream**](/windows/desktop/Stg/istream-compound-file-implementation)內的列印票證。<br/>        |
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | 將列印票證轉換成 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構。<br/>                                                                        |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | 抓取格式符合 XML [列印架構](./printschema.md)的印表機功能。<br/>                   |
| [**PTGetPrintDeviceCapabilities**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | 抓取裝置印表機的功能，其格式符合 XML [列印架構](./printschema.md)。<br/>            |
| [**PTGetPrintDeviceResources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | 它會針對格式符合 XML [列印架構](./printschema.md)的印表機抓取列印裝置資源。<br/> |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | 合併兩個列印票證，並傳回有效的可用列印票證。<br/>                                                                          |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | 開啟列印票證提供者的實例。<br/>                                                                                               |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | 開啟列印票證提供者的實例。<br/>                                                                                               |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | 抓取指定印表機支援之 [列印架構](./printschema.md) 的最高 (最新) 版本。<br/>           |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | 釋放與列印票證和列印功能相關聯的緩衝區。<br/>                                                                      |
| [**UnbindPTProviderThunk**](unbindptproviderthunk.md)<br/>                         | 關閉列印票證提供者的控制碼。<br/>                                                                                                 |



 

 

