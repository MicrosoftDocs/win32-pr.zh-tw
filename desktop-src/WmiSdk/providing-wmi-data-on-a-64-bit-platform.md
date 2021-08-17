---
description: 針對32位作業系統撰寫的腳本和應用程式應該會繼續正常執行。
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: 在64位平臺上提供 WMI 資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cb8a7e698723c6d4705a735591097fe7cf354db9684924d58f6b363c0ae6b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992638"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a>在64位平臺上提供 WMI 資料

針對32位作業系統撰寫的腳本和應用程式應該會繼續正常執行。 如果您有現有的32位提供者，您可以評估是否需要撰寫適用于並存作業的64位版本。 一般而言，這兩個版本都不是必要的，而且64位版本可以同時為32位和64位本機或遠端用戶端服務。 不過，若為32位應用程式相容性模式，請在以32位 WOW64 模式執行的64位系統上，使用現有的32位 WMI 提供者。

在罕見的情況下，32位和64位提供者必須並行在64位系統上執行。 在此情況下，所載入的適當提供者版本取決於呼叫端為32位或64位，以及本機或遠端。 使用連線物件內容旗標（ **\_ \_ microsoft.sqlserver.management.smo.wmi.wmiconnectioninfo.providerarchitecture<** 和 **\_ \_ RequiredArchitecture**）的呼叫端可以要求 WMI 載入非預設的提供者。 如需詳細資訊，請參閱 [在64位電腦上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)。

在不尋常的情況下，您必須並存執行32位和64位提供者，您必須確定已謹慎處理安裝和卸載案例。 這是因為 WMI 只有一個存放 [*庫*](gloss-w.md) ，而且32位和64位版本的 [**mofcomp.exe**](mofcomp.md) 將資料放在相同的存放庫中;32位或64位的 mof 檔案沒有任何差別。 重新安裝一個版本的提供者將不會造成損害：將會編譯 mof 檔案，並將類別儲存在存放庫中。 不過，刪除命名空間的第二個卸載可能會干擾其他提供者的作業。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在64位電腦上取得和提供資料](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[在64位平臺上要求 WMI 資料](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[將資料提供給 WMI](providing-data-to-wmi.md)
</dt> </dl>

 

 



