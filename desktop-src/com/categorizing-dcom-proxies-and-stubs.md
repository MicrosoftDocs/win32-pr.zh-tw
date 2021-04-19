---
title: 分類 DCOM proxy 和存根
description: 分類 DCOM proxy 和存根
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968936"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a><span data-ttu-id="320c2-103">分類 DCOM proxy 和存根</span><span class="sxs-lookup"><span data-stu-id="320c2-103">Categorizing DCOM Proxies and Stubs</span></span>

<span data-ttu-id="320c2-104">DCOM 會藉由建立包含 Clsid 的 OBJREFs 來封送處理物件的參考。</span><span class="sxs-lookup"><span data-stu-id="320c2-104">DCOM marshals references to objects by constructing OBJREFs that contain CLSIDs.</span></span> <span data-ttu-id="320c2-105">這些 Clsid 很容易受到安全性攻擊，因為封送處理期間可以載入任意 Dll。</span><span class="sxs-lookup"><span data-stu-id="320c2-105">These CLSIDs are vulnerable to security attacks because arbitrary DLLs can be loaded during marshaling.</span></span> <span data-ttu-id="320c2-106">不過，在 \_ \_ 呼叫 CoInitializeSecurity 時，不能指定 EOAC 的自訂 \_ 封送處理旗標 (請參閱 [**EOLE \_ 驗證 \_ 功能**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)) 。 [](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)</span><span class="sxs-lookup"><span data-stu-id="320c2-106">However, the EOAC\_NO\_CUSTOM\_MARSHAL flag can be specified when calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (see [**EOLE\_AUTHENTICATION\_CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span></span> <span data-ttu-id="320c2-107">設定此旗標可在使用 DCOM 時協助保護伺服器安全性，因為這樣可以減少執行任意 Dll 的機會。</span><span class="sxs-lookup"><span data-stu-id="320c2-107">Setting this flag helps protect server security when using DCOM because it reduces the chances of executing arbitrary DLLs.</span></span> <span data-ttu-id="320c2-108">當設定這個旗標時，伺服器只允許封送處理 ole32.dll、comadmin.dll、comsvcs.dll 或 es.dll 中所執行的 Clsid，或是執行 CATID \_ 封送處理器分類識別碼的 clsid。</span><span class="sxs-lookup"><span data-stu-id="320c2-108">When this flag is set, the server allows the marshaling only of CLSIDs that are implemented in ole32.dll, comadmin.dll, comsvcs.dll, or es.dll, or that implement the CATID\_MARSHALER category ID.</span></span>

<span data-ttu-id="320c2-109">CATID \_ 封送處理器是元件類別目錄 GUID，可以與已自訂封送處理的 CLSID 相關聯。</span><span class="sxs-lookup"><span data-stu-id="320c2-109">CATID\_MARSHALER is a component category GUID that can be associated with a CLSID that is being custom marshaled.</span></span> <span data-ttu-id="320c2-110">當 EOAC \_ 沒有透過 \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)設定自訂封送處理時，允許使用此 CLSID 進行自訂的介面進行封送處理。</span><span class="sxs-lookup"><span data-stu-id="320c2-110">The interfaces being custom marshaled with this CLSID are allowed when the EOAC\_NO\_CUSTOM\_MARSHAL is set via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="related-topics"></a><span data-ttu-id="320c2-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="320c2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="320c2-112">元件類別</span><span class="sxs-lookup"><span data-stu-id="320c2-112">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 