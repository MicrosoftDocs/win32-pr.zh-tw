---
title: 使用 System-Supplied 代理
description: 使用 System-Supplied 代理
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311390"
---
# <a name="using-the-system-supplied-surrogate"></a>使用 System-Supplied 代理

若要針對您的 DLL 伺服器使用系統提供的代理程式，請在登錄中註冊指定空字串或 **Null** 的 dll 以做為 [DllSurrogate](dllsurrogate.md) 值。 當 DLL 伺服器的啟用要求是針對 COM 而指定時，COM 會啟動預設的代理程式和要求的 DLL (方法是在內部) 的啟動命令列上指定 CLSID，以避免個別的呼叫。  (需在代理程式中執行多部 DLL 伺服器的詳細資訊，請參閱 [代理共用](surrogate-sharing.md)。 ) 

代理進程的預設實作為混合執行緒模型樣式的虛擬 COM 伺服器。 當多個 DLL 伺服器載入至單一代理程式時，此程式會使用該伺服器的登錄中指定的執行緒模型，確保每個 DLL 伺服器都具現化。 所有載入的自由執行緒伺服器都會在多執行緒單元中一起運作，而每個單元執行緒伺服器則會位於單一執行緒的單元中。 如果 DLL 伺服器同時支援這兩種執行緒模型，COM 將會選擇多執行緒處理。

寫入這個代理程式是為了讓 COM 處理卸載 DLL 伺服器和終止代理進程的作業。

系統提供的代理將非常適合大部分的開發人員，而且很容易使用。 不過，具有特殊考慮的開發人員可能會決定需要自訂的代理。 如需詳細資訊，請參閱 [撰寫自訂代理](writing-a-custom-surrogate.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DLL 代理](dll-surrogates.md)
</dt> </dl>

 

 




