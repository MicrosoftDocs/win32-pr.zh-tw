---
description: CNG 是一種加密 API，可讓您用來建立加密金鑰管理、加密和資料安全性，以及密碼編譯和網路安全性的加密安全性軟體。
ms.assetid: eaad88a1-4e1d-4246-9560-8eef60f8b70f
title: 密碼編譯 API：新一代
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d485f8371905961c63fbab66b29d0db544e3271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847669"
---
# <a name="cryptography-api-next-generation"></a><span data-ttu-id="2fbb5-103">密碼編譯 API：新一代</span><span class="sxs-lookup"><span data-stu-id="2fbb5-103">Cryptography API: Next Generation</span></span>

## <a name="purpose"></a><span data-ttu-id="2fbb5-104">目的</span><span class="sxs-lookup"><span data-stu-id="2fbb5-104">Purpose</span></span>

<span data-ttu-id="2fbb5-105">密碼編譯 API：新一代 (CNG) 是 [*CryptoAPI*](../secgloss/c-gly.md)的長期取代。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-105">Cryptography API: Next Generation (CNG) is the long-term replacement for the [*CryptoAPI*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2fbb5-106">CNG 的設計可在許多層級進行擴充，並在行為上進行中立性驗證。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-106">CNG is designed to be extensible at many levels and cryptography agnostic in behavior.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2fbb5-107">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="2fbb5-107">Developer audience</span></span>

<span data-ttu-id="2fbb5-108">CNG 適用于應用程式開發人員，這些應用程式可讓使用者在安全的環境中建立及交換檔和其他資料，尤其是在不安全的媒體（例如網際網路）上使用。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-108">CNG is intended for use by developers of applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="2fbb5-109">開發人員應該熟悉 C 和 c + + 程式設計語言和 Windows 型程式設計環境。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-109">Developers should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="2fbb5-110">雖然並非必要，但建議您瞭解密碼編譯或安全性相關的主題。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-110">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="2fbb5-111">如果您正在開發 CNG 密碼編譯演算法提供者或金鑰儲存提供者，則必須從 Microsoft 下載 [密碼編譯提供者開發工具組](https://www.microsoft.com/download/details.aspx?id=30688) 。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-111">If you are developing a CNG cryptographic algorithm provider or key storage provider, you must download the [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) from Microsoft.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2fbb5-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="2fbb5-112">Run-time requirements</span></span>

<span data-ttu-id="2fbb5-113">從 Windows Server 2008 和 Windows Vista 開始支援 CNG。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-113">CNG is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="2fbb5-114">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2fbb5-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="2fbb5-115">In this section</span></span>



| <span data-ttu-id="2fbb5-116">主題</span><span class="sxs-lookup"><span data-stu-id="2fbb5-116">Topic</span></span>                                         | <span data-ttu-id="2fbb5-117">描述</span><span class="sxs-lookup"><span data-stu-id="2fbb5-117">Description</span></span>                                                                                                                                    |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fbb5-118">關於 CNG</span><span class="sxs-lookup"><span data-stu-id="2fbb5-118">About CNG</span></span>](about-cng.md)<br/>         | <span data-ttu-id="2fbb5-119">描述 CNG 功能、密碼編譯基本專案，以及金鑰儲存、抓取、匯入和匯出。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-119">Describes CNG features, cryptographic primitives, and key storage, retrieval, import, and export.</span></span><br/>                                   |
| [<span data-ttu-id="2fbb5-120">使用 CNG</span><span class="sxs-lookup"><span data-stu-id="2fbb5-120">Using CNG</span></span>](using-cng.md)<br/>         | <span data-ttu-id="2fbb5-121">說明如何使用 CNG 和一般 CNG 程式設計的密碼編譯設定功能。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-121">Explains how to use the cryptography configuration features of CNG and typical CNG programming.</span></span><br/>                                     |
| [<span data-ttu-id="2fbb5-122">CNG 參考</span><span class="sxs-lookup"><span data-stu-id="2fbb5-122">CNG Reference</span></span>](cng-reference.md)<br/> | <span data-ttu-id="2fbb5-123">CNG 程式設計項目的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-123">Detailed descriptions of the CNG programming elements.</span></span> <span data-ttu-id="2fbb5-124">這些頁面包含使用 CNG 的 API 參考描述。</span><span class="sxs-lookup"><span data-stu-id="2fbb5-124">These pages include reference descriptions of the API for working with CNG.</span></span> <br/> |



 

 

