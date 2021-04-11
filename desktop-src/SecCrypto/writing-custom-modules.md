---
description: 您可以用 C、c + + 或 Visual Basic 程式設計語言撰寫原則模組。
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: 撰寫自訂模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944361"
---
# <a name="writing-custom-modules"></a><span data-ttu-id="1315e-103">撰寫自訂模組</span><span class="sxs-lookup"><span data-stu-id="1315e-103">Writing Custom Modules</span></span>

<span data-ttu-id="1315e-104">您可以用 C、c + + 或 Visual Basic 程式設計語言撰寫原則模組。</span><span class="sxs-lookup"><span data-stu-id="1315e-104">You can write policy modules in the C, C++, or Visual Basic programming language.</span></span> <span data-ttu-id="1315e-105">必要的 Microsoft 編譯器可在 Visual C++ 5.0 版或更新版本，或 Visual Basic 5.0 版或更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="1315e-105">The required Microsoft compiler is available in Visual C++ version 5.0 or later or in Visual Basic version 5.0 or later.</span></span> <span data-ttu-id="1315e-106"> (CA) 的企業 [*憑證授權單位*](../secgloss/c-gly.md) 單位只能使用 Microsoft 提供的企業原則模組。</span><span class="sxs-lookup"><span data-stu-id="1315e-106">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

<span data-ttu-id="1315e-107">撰寫自訂原則模組時，您必須執行 [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) 。</span><span class="sxs-lookup"><span data-stu-id="1315e-107">You must implement [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) when writing a custom policy module.</span></span> <span data-ttu-id="1315e-108">此外，撰寫自訂原則模組時，您必須執行 [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) 。</span><span class="sxs-lookup"><span data-stu-id="1315e-108">Additionally, you must implement [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) when writing a custom policy module.</span></span>

<span data-ttu-id="1315e-109">原則模組可以從 [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) 呼叫方法，以協助處理 [*憑證要求*](../secgloss/c-gly.md); **ICertServerPolicy** 可讓您設定和抓取屬性和憑證延伸。</span><span class="sxs-lookup"><span data-stu-id="1315e-109">Policy modules can call methods from [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) to assist in the processing of a [*certificate request*](../secgloss/c-gly.md); **ICertServerPolicy** allows properties and certificate extensions to be set and retrieved.</span></span>

<span data-ttu-id="1315e-110">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="1315e-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="1315e-111">主題</span><span class="sxs-lookup"><span data-stu-id="1315e-111">Topic</span></span>                                                                      | <span data-ttu-id="1315e-112">描述</span><span class="sxs-lookup"><span data-stu-id="1315e-112">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="1315e-113">設定憑證屬性</span><span class="sxs-lookup"><span data-stu-id="1315e-113">Setting Certificate Properties</span></span>](setting-certificate-properties.md)       | <span data-ttu-id="1315e-114">設定憑證的屬性</span><span class="sxs-lookup"><span data-stu-id="1315e-114">Setting the properties of a certificate</span></span> |
| [<span data-ttu-id="1315e-115">撰寫自訂結束模組</span><span class="sxs-lookup"><span data-stu-id="1315e-115">Writing Custom Exit Modules</span></span>](writing-custom-exit-modules.md)             | <span data-ttu-id="1315e-116">撰寫自訂結束模組</span><span class="sxs-lookup"><span data-stu-id="1315e-116">Writing custom exit modules</span></span>             |
| [<span data-ttu-id="1315e-117">撰寫自訂延伸模組處理常式</span><span class="sxs-lookup"><span data-stu-id="1315e-117">Writing Custom Extension Handlers</span></span>](writing-custom-extension-handlers.md) | <span data-ttu-id="1315e-118">撰寫自訂延伸模組處理常式</span><span class="sxs-lookup"><span data-stu-id="1315e-118">Writing custom extension handlers</span></span>       |



 

 

 
