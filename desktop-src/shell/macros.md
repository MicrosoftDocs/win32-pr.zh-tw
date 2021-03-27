---
description: 本節說明 Windows Shell 公用程式宏。
title: Shell 宏
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 085bca918cfa6ca1441272c3c9181226ef603ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944498"
---
# <a name="shell-macros"></a>Shell 宏

本節說明 Windows Shell 公用程式宏。

## <a name="in-this-section"></a>本節內容



| 主題                                                                  | 描述                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**定義 \_ PROPERTYKEY**](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | 用來封裝格式識別碼 (FMTID) 和屬性識別碼 (PID) 為代表屬性索引鍵的 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) 結構。<br/>                                                                                    |
| [**IID \_ PPV 引數 \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | 用來取出介面指標，並根據所使用介面指標的類型，自動提供所要求介面的 IID 值。 藉由檢查編譯時期傳遞的數值型別，即可避免常見的編碼錯誤。<br/> |
| [**IsEqualPropertyKey**](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | 比較兩個 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) 結構的成員，並傳回兩者是否相等。<br/>                                                                                                                                 |
| [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | 用來將 DLL 版本資訊封裝成 ULONGLONG 值。<br/>                                                                                                                                                                                         |
| [**NetAddr \_ DisplayErrorTip**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | 在與網路位址控制項相關聯的氣球提示中顯示錯誤訊息。<br/>                                                                                                                                                            |
| [**NetAddr \_ GetAddress**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | 指出網路位址是否符合指定的類型和格式。<br/>                                                                                                                                                                         |
| [**NetAddr \_ GetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | 抓取指定的網路位址控制項接受的網路位址類型。<br/>                                                                                                                                                                |
| [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | 設定指定的網路位址控制項接受的網路位址類型。<br/>                                                                                                                                                                     |



 

 

 
