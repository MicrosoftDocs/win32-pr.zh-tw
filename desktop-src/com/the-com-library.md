---
title: COM 程式庫
description: COM 程式庫
ms.assetid: 51d4db4a-ad88-4627-8140-2f7906945752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50de440e931d2de381290f0167d146768d89fe66b7cfa0d2abbc43624521d21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103800"
---
# <a name="the-com-library"></a>COM 程式庫

任何使用 COM 的進程都必須初始化和解除初始化 COM 程式庫。 除了做為規格之外，COM 也會在此程式庫中實行一些重要的服務。 以一組 dll 和 exe 的形式提供 (主要是在 Microsoft Windows 中 Ole32.dll 和 Rpcss.exe) ，COM 程式庫包含下列各項：

-   許多基本功能，可協助建立 COM 應用程式（用戶端和伺服器）。 針對用戶端，COM 會提供基本功能來建立物件。 針對伺服器，COM 會提供公開其物件的方法。

-   由 COM 從唯一類別識別碼 (CLSID) 的實作為定位器服務，該服務會在伺服器上執行該類別以及該伺服器所在位置。 這項服務包括在物件類別的身分識別與執行封裝之間的間接取值層級（通常是系統登錄）之間的支援，以便用戶端與封裝無關（未來可能會變更）。

-   當物件在本機或遠端伺服器中執行時，透明的遠端程序呼叫。

-   一種標準機制，可讓應用程式控制在其進程內配置記憶體的方式，特別是需要在合作物件之間傳遞的記憶體，才能正確釋放記憶體。

若要使用基本 COM 服務，在用戶端和跨進程伺服器中執行的所有 COM 執行緒都必須呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) 函式，然後再呼叫其他任何 COM 函式，但記憶體配置呼叫除外。 **CoInitializeEx** 會取代另一個函式，加入可讓您指定執行緒執行緒模型的參數：「跨執行緒」或「無限制執行緒」。 對 **CoInitialize** 的呼叫只會將執行緒模型設定為單元執行緒。

OLE 複合檔案應用程式會呼叫 [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize) 函式，此函式會呼叫 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ，也會執行複合檔案所需的部分初始化。 因此，呼叫 **OleInitialize** 的執行緒不能自由執行緒。 如需用戶端和伺服器中線程的詳細資訊，請參閱 [進程、執行緒和單元](processes--threads--and-apartments.md)。

同進程伺服器不會呼叫初始化函式，因為它們會載入至已完成的處理常式。 因此，同進程伺服器必須在登錄中的 [InprocServer32](inprocserver32.md) 機碼下設定其執行緒模型。 如需有關同進程伺服器中線程問題的詳細資訊，請參閱同進程 [伺服器執行緒問題](in-process-server-threading-issues.md)。

解除初始化程式庫也很重要。 對於每個 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)的呼叫，都必須有對應的 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)呼叫。 對於 [**OleInitialize**](/windows/desktop/api/Ole2/nf-ole2-oleinitialize)的每個呼叫，都必須有對應的 [**OleUninitialize**](/windows/desktop/api/Ole2/nf-ole2-oleuninitialize)呼叫。

同進程伺服器可以假設它們正在載入的進程已執行這些步驟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件物件模型](the-component-object-model.md)
</dt> </dl>

 

 




