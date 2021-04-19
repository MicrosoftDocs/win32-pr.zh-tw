---
description: 密碼編譯 API：新一代 (CNG) 定義與 CNG 密碼編譯配置系統搭配使用的下列功能。
ms.assetid: 45936528-ee29-4bc5-a609-4ca53cd08da7
title: CNG 密碼編譯設定函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30811e94aabeddb88e7c10251e1206768f891d17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966671"
---
# <a name="cng-cryptographic-configuration-functions"></a><span data-ttu-id="8f9a2-103">CNG 密碼編譯設定函數</span><span class="sxs-lookup"><span data-stu-id="8f9a2-103">CNG Cryptographic Configuration Functions</span></span>

<span data-ttu-id="8f9a2-104">密碼編譯 API：新一代 (CNG) 定義與 CNG 密碼編譯配置系統搭配使用的下列功能。</span><span class="sxs-lookup"><span data-stu-id="8f9a2-104">Cryptography API: Next Generation (CNG) defines the following functions that are used with the CNG cryptographic configuration system.</span></span>

-   [<span data-ttu-id="8f9a2-105">**BCryptAddCoNtextFunction**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-105">**BCryptAddContextFunction**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptaddcontextfunction)
-   [<span data-ttu-id="8f9a2-106">**BCryptConfigureCoNtext**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-106">**BCryptConfigureContext**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptconfigurecontext)
-   [<span data-ttu-id="8f9a2-107">**BCryptConfigureCoNtextFunction**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-107">**BCryptConfigureContextFunction**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptconfigurecontextfunction)
-   [<span data-ttu-id="8f9a2-108">**BCryptCreateCoNtext**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-108">**BCryptCreateContext**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatecontext)
-   [<span data-ttu-id="8f9a2-109">**BCryptDeleteCoNtext**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-109">**BCryptDeleteContext**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdeletecontext)
-   [<span data-ttu-id="8f9a2-110">**BCryptEnumAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-110">**BCryptEnumAlgorithms**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumalgorithms)
-   [<span data-ttu-id="8f9a2-111">**BCryptEnumCoNtextFunctionProviders**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-111">**BCryptEnumContextFunctionProviders**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumcontextfunctionproviders)
-   [<span data-ttu-id="8f9a2-112">**BCryptEnumCoNtextFunctions**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-112">**BCryptEnumContextFunctions**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumcontextfunctions)
-   [<span data-ttu-id="8f9a2-113">**BCryptEnumCoNtexts**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-113">**BCryptEnumContexts**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumcontexts)
-   [<span data-ttu-id="8f9a2-114">**BCryptEnumProviders**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-114">**BCryptEnumProviders**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumproviders)
-   [<span data-ttu-id="8f9a2-115">**BCryptEnumRegisteredProviders**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-115">**BCryptEnumRegisteredProviders**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders)
-   [<span data-ttu-id="8f9a2-116">**BCryptGetFipsAlgorithmMode**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-116">**BCryptGetFipsAlgorithmMode**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetfipsalgorithmmode)
-   [<span data-ttu-id="8f9a2-117">**BCryptQueryCoNtextConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-117">**BCryptQueryContextConfiguration**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptquerycontextconfiguration)
-   [<span data-ttu-id="8f9a2-118">**BCryptQueryCoNtextFunctionConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-118">**BCryptQueryContextFunctionConfiguration**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptquerycontextfunctionconfiguration)
-   [<span data-ttu-id="8f9a2-119">**BCryptQueryCoNtextFunctionProperty**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-119">**BCryptQueryContextFunctionProperty**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptquerycontextfunctionproperty)
-   [<span data-ttu-id="8f9a2-120">**BCryptQueryProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-120">**BCryptQueryProviderRegistration**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration)
-   [<span data-ttu-id="8f9a2-121">**BCryptRegisterConfigChangeNotify (控制碼 \*)**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-121">**BCryptRegisterConfigChangeNotify(HANDLE\*)**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify)
-   [<span data-ttu-id="8f9a2-122">**BCryptRegisterConfigChangeNotify (PRKEVENT)**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-122">**BCryptRegisterConfigChangeNotify(PRKEVENT)**</span></span>](/windows/win32/api/bcrypt/nf-bcrypt-bcryptregisterconfigchangenotify)
-   [<span data-ttu-id="8f9a2-123">**BCryptRemoveCoNtextFunction**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-123">**BCryptRemoveContextFunction**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptremovecontextfunction)
-   [<span data-ttu-id="8f9a2-124">**BCryptResolveProviders**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-124">**BCryptResolveProviders**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptresolveproviders)
-   [<span data-ttu-id="8f9a2-125">**BCryptSetCoNtextFunctionProperty**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-125">**BCryptSetContextFunctionProperty**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetcontextfunctionproperty)
-   [<span data-ttu-id="8f9a2-126">**BCryptUnregisterConfigChangeNotify (控制碼)**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-126">**BCryptUnregisterConfigChangeNotify(HANDLE)**</span></span>](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptunregisterconfigchangenotify)
-   [<span data-ttu-id="8f9a2-127">**BCryptUnregisterConfigChangeNotify (PRKEVENT)**</span><span class="sxs-lookup"><span data-stu-id="8f9a2-127">**BCryptUnregisterConfigChangeNotify(PRKEVENT)**</span></span>](/windows/win32/api/bcrypt/nf-bcrypt-bcryptunregisterconfigchangenotify)

 

 
