---
title: ADSI 擴充功能架構
description: ADSI 擴充功能是以 COM 匯總模型為基礎，具有數個增強功能。 擴充功能必須遵守所有 COM 規則。 如需詳細資訊，請參閱 COM 規格。
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- 延伸模組 ADSI、延伸模組架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239a2562054f062464fc924a0f67c31ea3d9fab696fd23e532eab78e1dc66d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023862"
---
# <a name="adsi-extension-architecture"></a>ADSI 擴充功能架構

ADSI 擴充功能是以 COM 匯總模型為基礎，具有數個增強功能。 擴充功能必須遵守所有 COM 規則。 如需詳細資訊，請參閱 COM 規格。

以下是 COM 匯總模型的評論。

![com 匯總模型](images/comagmod.png)

匯總（也稱為內建物件）是匯總工具所建立的物件。 您的擴充物件是匯總。

匯總工具（也稱為外部物件）是建立匯總的物件。 ADSI 是一個匯總工具。

內建物件會將其 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 委派給匯總工具的 **iunknown**。

ADSI 擴充功能會將下列增強功能新增至 COM 匯總，以滿足其需求：

-   可讓每個延伸模組寫入器擴充 ADSI 物件。 延伸模組寫入器可以使用 ADSI 註冊它的擴充功能，而不會受到其他副檔名的存在影響。 在 COM 匯總模型中，匯總工具必須有匯總的 CLSID。 ADSI 會放寬這項需求，使其成為所有延伸模組的匯總工具。 因此，延伸模組會位於相同層級，而不是形成一層嵌套的元件。
-   允許一個物件，一個 IDispatch。 自動化支援是 ADSI 最重要的功能之一。 因為 ADSI 支援 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面，所以可達成自動化支援。 建議延伸模組寫入器支援 **IDispatch** 介面。 不過，指定的物件上應該只有一個 **IDispatch** 介面。 ADSI 整合並收集不同擴充功能的許多 **IDispatch** 介面，並將其顯示為自動化控制器的一個一致 **idispatch** 。 每個擴充功能在匯總時，都必須將其 **idispatch** 呼叫重新路由傳送至 ADSI 所提供的 **idispatch** 。

由於 ADSI 物件管理員提供的服務（位於每個 ADSI 提供者上），因此這些解決方案都是可行的。

下圖顯示 ADSI 擴充功能模型架構。

![adsi 擴充模型架構](images/adsiexmo.png)

ADSI 支援兩種層級的延伸模組：

-   早期繫結支援。 這是延伸模組的第一個層級。 延伸模組必須支援註冊和執行新的介面。 擴充功能取用者必須使用支援早期繫結的工具或腳本主機，例如 Visual C++ Visual Basic。
-   晚期繫結支援。 當延伸模組滿足所有早期繫結需求，並執行額外的介面 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)時，就會發生這種情況。 延伸模組實作者可以使用任何以 Automation 控制器運作的工具，例如 Windows 腳本主機、使用中的伺服器頁，或使用 VBScript 的 HTML。

 

 