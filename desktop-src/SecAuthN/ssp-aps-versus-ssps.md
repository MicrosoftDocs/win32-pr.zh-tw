---
description: 說明 SSP/Ap 與 Ssp 之間的差異。
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/Ap 與 Ssp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944881"
---
# <a name="sspaps-vs-ssps"></a><span data-ttu-id="52b0b-103">SSP/Ap 與 Ssp</span><span class="sxs-lookup"><span data-stu-id="52b0b-103">SSP/APs vs. SSPs</span></span>

<span data-ttu-id="52b0b-104">[*安全性套件*](../secgloss/s-gly.md) 會以下列其中一種動態連結程式庫類型部署 (dll) ：</span><span class="sxs-lookup"><span data-stu-id="52b0b-104">[*Security packages*](../secgloss/s-gly.md) are deployed in one of the following types of dynamic-link libraries (DLLs):</span></span>

-   [<span data-ttu-id="52b0b-105">SSP/Ap</span><span class="sxs-lookup"><span data-stu-id="52b0b-105">SSP/APs</span></span>](#sspaps-vs-ssps)
-   [<span data-ttu-id="52b0b-106">Ssp</span><span class="sxs-lookup"><span data-stu-id="52b0b-106">SSPs</span></span>](#sspaps-vs-ssps)

<span data-ttu-id="52b0b-107">安全性套件是否位於安全性支援提供者/[*驗證套件*](../secgloss/a-gly.md) (SSP/AP) 或 [*安全性支援提供者*](../secgloss/s-gly.md) (ssp) DLL 是由它所提供的安全性服務類型以及它需要與 [*本地安全機構*](../secgloss/l-gly.md) (LSA) 整合的程度決定。</span><span class="sxs-lookup"><span data-stu-id="52b0b-107">Whether a security package is in a security support provider/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) or a [*security support provider*](../secgloss/s-gly.md) (SSP) DLL is determined by the types of security services it provides and the extent to which it requires integration with the [*Local Security Authority*](../secgloss/l-gly.md) (LSA).</span></span> <span data-ttu-id="52b0b-108">這些差異也會決定在自訂安全性封裝中實作為的 API。</span><span class="sxs-lookup"><span data-stu-id="52b0b-108">These differences also determine the API implemented in a custom security package.</span></span>

## <a name="sspaps"></a><span data-ttu-id="52b0b-109">SSP/Ap</span><span class="sxs-lookup"><span data-stu-id="52b0b-109">SSP/APs</span></span>

<span data-ttu-id="52b0b-110">SSP/AP 是包含一或多個 [*安全性套件*](../secgloss/s-gly.md) 的 DLL，可以作為用戶端/伺服器應用程式的 SSP，以及做為登入應用程式的 [驗證套件](authentication-packages.md) 。</span><span class="sxs-lookup"><span data-stu-id="52b0b-110">An SSP/AP is a DLL that contains one or more [*Security packages*](../secgloss/s-gly.md) and can function as an SSP for client/server applications and as an [authentication package](authentication-packages.md) for logon applications.</span></span> <span data-ttu-id="52b0b-111">為了在這兩個角色中運作，SSP/Ap 會在系統啟動時載入至 LSA 進程空間，也可以載入至用戶端/伺服器應用程式進程。</span><span class="sxs-lookup"><span data-stu-id="52b0b-111">To function in both of these roles, SSP/APs are loaded into the LSA process space at system startup and can be loaded into client/server application processes as well.</span></span>

<span data-ttu-id="52b0b-112">自訂 SSP/AP 安全性套件必須同時執行 [由使用者模式 SSP/ap 所執行](authentication-functions.md)的函式，以及 [由 SSP/ap 所執行](authentication-functions.md)的函式。</span><span class="sxs-lookup"><span data-stu-id="52b0b-112">Custom SSP/AP security packages must implement both the [Functions Implemented by User-mode SSP/APs](authentication-functions.md), and [Functions Implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="52b0b-113">這些函式的使用方式可以利用 LSA 支援函式來提供先進的安全性功能，例如權杖建立、 [*補充*](../secgloss/s-gly.md) 認證支援和傳遞驗證。</span><span class="sxs-lookup"><span data-stu-id="52b0b-113">These function implementations can make use of LSA support functions to offer advanced security features such as token creation, [*supplemental credentials*](../secgloss/s-gly.md) support, and pass-through authentication.</span></span>

<span data-ttu-id="52b0b-114">如果自訂的 SSP/AP 安全性套件提供完整範圍的訊息 [*完整性*](../secgloss/i-gly.md) 和隱私權功能，也會執行 [由使用者模式 SSP/ap 所執行](authentication-functions.md)的函式。</span><span class="sxs-lookup"><span data-stu-id="52b0b-114">If a custom SSP/AP security package provides the full range of message [*integrity*](../secgloss/i-gly.md) and privacy functions, it will also implement the [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span>

## <a name="ssps"></a><span data-ttu-id="52b0b-115">Ssp</span><span class="sxs-lookup"><span data-stu-id="52b0b-115">SSPs</span></span>

<span data-ttu-id="52b0b-116">SSP 是一個包含一或多個安全性套件的 DLL，可為用戶端/伺服器應用程式提供已驗證的連線、訊息完整性和訊息加密服務。</span><span class="sxs-lookup"><span data-stu-id="52b0b-116">An SSP is a DLL that contains one or more security packages that provide authenticated connection, message integrity, and message encryption services to client/server applications.</span></span> <span data-ttu-id="52b0b-117">Ssp (SSPI) 函式來實行 [安全性支援提供者介面](sspi.md) 。</span><span class="sxs-lookup"><span data-stu-id="52b0b-117">SSPs implement [Security Support Provider Interface](sspi.md) (SSPI) functions.</span></span> <span data-ttu-id="52b0b-118">應用程式可以直接呼叫 SSPI 函式，以存取 SSP 中的安全性套件。</span><span class="sxs-lookup"><span data-stu-id="52b0b-118">Applications can access the security packages in an SSP by calling the SSPI functions directly.</span></span> <span data-ttu-id="52b0b-119">Ssp 會載入至用戶端和伺服器進程;它們不會與 LSA 整合。</span><span class="sxs-lookup"><span data-stu-id="52b0b-119">SSPs are loaded into the client and server processes; they are not integrated with the LSA.</span></span>

 

 
