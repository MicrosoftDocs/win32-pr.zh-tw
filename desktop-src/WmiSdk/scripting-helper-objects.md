---
description: WMI 有數個腳本 helper 物件，可提供腳本所需的轉換。
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: 腳本 Helper 物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974380"
---
# <a name="scripting-helper-objects"></a>腳本 Helper 物件

WMI 有數個腳本 helper 物件，可提供腳本所需的轉換。

WMI 腳本 helper 物件包括：

-   [**SWbemDateTime**](swbemdatetime.md)
-   [**SWbemObjectPath**](swbemobjectpath.md)
-   [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

Helper 物件會細分複合資料結構，因此不需要腳本來剖析結構以取得任何片段。 例如， **WMI DATETIME** 結構無法直接顯示，與其他 Windows DATETIME 資料結構（例如 **VT \_ DATE**）不同。

## <a name="swbemdatetime"></a>SWbemDateTime

[**SWbemDateTime**](swbemdatetime.md)物件提供的屬性會剖析出日、月、年、一天中的時間等等。 它也提供轉換方法，以將 Windows Management Instrumentation (WMI) datetime 轉換成 **VT \_ 日期** 和 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 格式。 針對 Internet Explorer (IE) 安全性設定， **SWbemDateTime** 物件是唯一標示為 safe 以進行初始化的 WMI 腳本物件，以及可安全的腳本處理。 如需日期和時間轉換的詳細資訊和範例，請參閱有關「日期 [和](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) 時間」以及有關 TechNet ScriptCenter 的文章，也就 [是 (喔的時間，以及日期的) ](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx)。

## <a name="swbemobjectpath"></a>SWbemObjectPath

[**SWbemObjectPath**](swbemobjectpath.md)的屬性提供物件的絕對路徑，但也會細分 WMI 路徑的部分，例如伺服器、命名空間、類別或相對路徑。 物件可讓您設定路徑的安全性、取得代表路徑之物件的索引鍵值、判斷物件是否為 singleton，依此類推。 如需使用 WMI 物件路徑的詳細資訊，請參閱 [描述 Wmi 物件的位置](describing-the-location-of-a-wmi-object.md)。

## <a name="win32_securitydescriptorhelper"></a>Win32 \_ SecurityDescriptorHelper

[**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)類別會將安全物件的安全描述項從某種格式轉換成另一種格式。

許多物件（例如印表機、WMI 命名空間、登錄機碼或 DCOM 應用程式）都有安全描述項可控制物件的存取權。 您可以藉由取得或設定與物件相關聯的安全描述項，使用 WMI 來探索或變更可存取這些物件的人員。

不過，不同的方法可能會取得二進位位元組陣列中的安全描述項、 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-string-format) (SDDL) 格式，或作為 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的實例。 除了針對 [安全描述項作業](/windows/desktop/SecAuthZ/security-descriptor-operations)而設計的 c + + 方法以外，不應操作安全描述項的二進位位元組陣列形式。 SDDL 中的描述元是在字串中，但仍很難操作。 最簡單的操作格式是 **Win32 \_ SecurityDescriptor**，因為它包含信任者、ACE 和 SID 的内嵌物件。 如需 WMI 中安全描述項結構的詳細資訊，請參閱 [Wmi 安全描述項物件](wmi-security-descriptor-objects.md)。 如需如何進行轉換的詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
