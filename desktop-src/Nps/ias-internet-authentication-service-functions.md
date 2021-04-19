---
title: NPS 擴充功能函式
description: NPS 擴充功能函式
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "107001283"
---
# <a name="nps-extensions-functions"></a>NPS 擴充功能函式

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

## <a name="application-defined"></a>定義的應用程式

NPS 擴充功能 Dll 的架構支援下列匯出的函式：

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

[**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)和 [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)函數是選擇性的。

延伸模組 DLL 可以匯出 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) ，而不是 [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) 或 [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)。

如果延伸模組 DLL 匯出 [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)，則它也必須匯出 [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)。

## <a name="system-defined"></a>系統定義

當 NPS 呼叫 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)的執行時，nps 會將指標傳遞至 [**RADIUS \_ 延伸 \_ \_ 模組控制區塊**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) 結構的指標。

[**RADIUS \_ 延伸 \_ 模組控制 \_ 區塊**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block)結構包含 NPS 所提供之下列函式的函式指標：

-   [**GetRequest**](/previous-versions/ms688263(v=vs.85))
-   [**GetResponse**](/previous-versions/ms688270(v=vs.85))
-   [**SetResponseType**](/previous-versions/ms688462(v=vs.85))

[**GetRequest**](/previous-versions/ms688263(v=vs.85))和 [**GetResponse**](/previous-versions/ms688270(v=vs.85))函式會傳回 [**RADIUS \_ 屬性 \_ 陣列**](/windows/desktop/api/authif/ns-authif-radius_attribute_array)類型之結構的指標。

[**RADIUS \_ 屬性 \_ 陣列**](/windows/desktop/api/authif/ns-authif-radius_attribute_array)結構包含 NPS 所提供之下列函式的函式指標：

-   [**加入**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize**](/previous-versions/ms688277(v=vs.85))
-   [**InsertAt**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 