---
title: BITS c + + 應用程式範例
description: 本節中) 應用程式範例背景智慧型傳送服務 (位是以 c + + 撰寫。 它們示範可以使用 BITS 功能來完成的各種工作。 每個應用程式都分成一系列的步驟。
ms.assetid: 6163c7fd-e187-4f75-bf25-e3a515e50db5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf577509dac58a655c2cbc8b602b75bd48aa03e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023845"
---
# <a name="bits-c-application-examples"></a><span data-ttu-id="8cce1-105">BITS c + + 應用程式範例</span><span class="sxs-lookup"><span data-stu-id="8cce1-105">BITS C++ Application Examples</span></span>

<span data-ttu-id="8cce1-106">本節中) 應用程式範例背景智慧型傳送服務 (位是以 c + + 撰寫。</span><span class="sxs-lookup"><span data-stu-id="8cce1-106">The Background Intelligent Transfer Service (BITS) application examples in this section are written in C++.</span></span> <span data-ttu-id="8cce1-107">它們示範可以使用 BITS 功能來完成的各種工作。</span><span class="sxs-lookup"><span data-stu-id="8cce1-107">They demonstrate a range of tasks that can be completed by using BITS features.</span></span> <span data-ttu-id="8cce1-108">每個應用程式都分成一系列的步驟。</span><span class="sxs-lookup"><span data-stu-id="8cce1-108">Each application is separated into a series of steps.</span></span>

<span data-ttu-id="8cce1-109">下表列出本節中的 c + + 範例。</span><span class="sxs-lookup"><span data-stu-id="8cce1-109">The following table lists the C++ examples in this section.</span></span>



| <span data-ttu-id="8cce1-110">範例</span><span class="sxs-lookup"><span data-stu-id="8cce1-110">Example</span></span>                                                                                                                                                            | <span data-ttu-id="8cce1-111">描述</span><span class="sxs-lookup"><span data-stu-id="8cce1-111">Description</span></span>                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cce1-112">範例：通用類別</span><span class="sxs-lookup"><span data-stu-id="8cce1-112">Example: Common Classes</span></span>](common-classes.md)                                                                                                                      | <span data-ttu-id="8cce1-113">此範例包含用於本節中範例的一般類別。</span><span class="sxs-lookup"><span data-stu-id="8cce1-113">This example contains common classes that are used for the examples in this section.</span></span> <span data-ttu-id="8cce1-114">這些常見的類別包括回呼類別、泛型錯誤類別，以及 COM [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 函式的資源取得協助程式類別。</span><span class="sxs-lookup"><span data-stu-id="8cce1-114">These common classes include a callback class, a generic error class, and a resource acquisition helper class for the COM [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> |
| [<span data-ttu-id="8cce1-115">範例：指定 BITS 傳送工作的伺服器驗證認證</span><span class="sxs-lookup"><span data-stu-id="8cce1-115">Example: Specifying Server Authentication Credentials for a BITS Transfer Job</span></span>](example-specifying-server-authentication-credentials-for-a-bits-transfer-job-.md) | <span data-ttu-id="8cce1-116">此範例會取得使用者的授權配置和認證、建立 BITS 傳送工作、設定作業的認證，以及監視作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="8cce1-116">This example gets the authorization scheme and credentials from the user, creates a BITS transfer job, sets the credentials for the job, and monitors the status of the job.</span></span>                                                                                                               |
| [<span data-ttu-id="8cce1-117">範例：搭配使用 SSPI 驗證編碼和 BITS。</span><span class="sxs-lookup"><span data-stu-id="8cce1-117">Example: Using SSPI Authentication Encoding with BITS.</span></span>](example-using-sspi-authentication-encoding-with-bits.md)                                                 | <span data-ttu-id="8cce1-118">此範例示範如何使用安全性支援提供者介面 (SSPI) 驗證和 BITS 來取得使用者的認證、將認證編碼，以及在 BITS 傳送工作上設定編碼的認證。</span><span class="sxs-lookup"><span data-stu-id="8cce1-118">This example demonstrates the use of Security Support Provider Interface (SSPI) authentication and BITS to get the credentials from a user, encode the credentials, and set the encoded credentials on a BITS transfer job.</span></span>                                                                |
| [<span data-ttu-id="8cce1-119">範例：將 Helper 權杖新增至 BITS 傳送工作</span><span class="sxs-lookup"><span data-stu-id="8cce1-119">Example: Adding a Helper Token to a BITS Transfer Job</span></span>](example-adding-a-helper-token-to-a-bits-transfer-job-.md)                                                 | <span data-ttu-id="8cce1-120">這個範例會建立 BITS 傳送工作，並將第二組認證新增至作業。</span><span class="sxs-lookup"><span data-stu-id="8cce1-120">This example creates a BITS transfer job and adds a second set of credentials to the job.</span></span>                                                                                                                                                                                                  |



 

 

 