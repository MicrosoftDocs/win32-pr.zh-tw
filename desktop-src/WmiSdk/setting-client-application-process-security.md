---
description: 呼叫 WMI 介面的用戶端應用程式可以控制其進程的安全性層級。
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: 設定用戶端應用程式處理安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be6b3f6e632ade53700bbe81afc7698a06fe2ff038e0c57c1b4a7eed44afa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739466"
---
# <a name="setting-client-application-process-security"></a>設定用戶端應用程式處理安全性

呼叫 WMI 介面的用戶端應用程式可以控制其進程的安全性層級。 所有 WMI 應用程式都會透過 COM 存取 WMI，而您可以呼叫 COM 函式 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 來設定處理常式的安全性。 對 WMI 進行非同步呼叫的應用程式，以及註冊為事件取用者的應用程式，會將呼叫的安全性層級設定為 WMI。

如果您沒有明確呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)，COM 會以隱含方式呼叫登錄中的值。 但是，登錄值可能會有較低的模擬和驗證設定，而不會提供 WMI 所需的安全性。 如需詳細資訊，請參閱 [使用 c + + 設定預設進程安全性層級](setting-the-default-process-security-level-using-c-.md)。

不建議對 WMI 進行非同步存取。 非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用最半同步或同步通訊，或在用戶端應用程式中執行適當的存取檢查。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

對任何 WMI proxy 的呼叫 ([**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)、 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)、[**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)或 [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) 使用跨進程指標。 如需預設值和建議的詳細資訊，請參閱 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。

下列程式說明在應用程式處理常式上設定 WMI 安全性時必須執行的步驟。

**若要設定應用程式進程上的 WMI 安全性**

1.  判斷用戶端應用程式執行所在的 Windows 作業系統所需的安全性層級。
2.  呼叫 COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函式，以設定用戶端應用程式執行所在之進程的預設安全性。 這會宣告其他應用程式在應用程式執行時需要多少安全性。
3.  如果您需要變更個別 proxy 的安全性（例如，在另一次呼叫 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)時），請呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)。
4.  如果您需要控制遠端硬體或需要更多許可權的系統物件，請使用 [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函式來啟用必要的許可權。 請注意，您無法啟用尚未指派處理常式的許可權。 如需詳細資訊，請參閱 [檢查私用物件的存取權](/windows/desktop/SecAuthZ/checking-access-to-private-objects)。

如需設定預設進程安全性等級的詳細資訊，請參閱使用 [c + + 設定預設進程安全性等級](setting-the-default-process-security-level-using-c-.md) 和 [使用 VBScript 設定預設進程安全性層](setting-the-default-process-security-level-using-vbscript.md)級。

 

 
