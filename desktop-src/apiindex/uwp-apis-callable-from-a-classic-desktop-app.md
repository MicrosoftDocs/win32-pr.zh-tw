---
description: 一般規則是桌面應用程式可以呼叫 Windows 執行階段 (WinRT) API。 不過，某些 Api （包括 XAML UI Api）要求呼叫應用程式必須有套件身分識別。
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: 從桌面應用程式呼叫的 WinRT Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9083fbfb16391c626f49b79176fed7a81068c028
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2020
ms.locfileid: "104024319"
---
# <a name="calling-winrt-apis-from-a-desktop-app"></a><span data-ttu-id="4a19c-104">從桌面應用程式呼叫 WinRT Api</span><span class="sxs-lookup"><span data-stu-id="4a19c-104">Calling WinRT APIs from a desktop app</span></span>

<span data-ttu-id="4a19c-105">一般規則是桌面應用程式可以呼叫 WinRT API。</span><span class="sxs-lookup"><span data-stu-id="4a19c-105">The general rule is that a desktop app can call a WinRT API.</span></span> <span data-ttu-id="4a19c-106">不過，某些 Api （包括 XAML UI Api）要求呼叫應用程式必須有套件身分識別。</span><span class="sxs-lookup"><span data-stu-id="4a19c-106">However, some APIs, including the XAML UI APIs, require the calling app to have a package identity.</span></span> <span data-ttu-id="4a19c-107">UWP 應用程式具有妥善定義的應用程式模型，且具有套件身分識別。</span><span class="sxs-lookup"><span data-stu-id="4a19c-107">UWP apps have a well-defined app model, and they have a package identity.</span></span> <span data-ttu-id="4a19c-108">其他類型的桌面應用程式都沒有妥善定義的應用程式模型，也沒有套件身分識別。</span><span class="sxs-lookup"><span data-stu-id="4a19c-108">The other types of desktop apps have neither a well-defined app model, nor a package identity.</span></span> <span data-ttu-id="4a19c-109">因此，如果 API 需要套件身分識別，WPF、Windows Forms 或 Win32 應用程式就無法呼叫它，除非應用程式 [封裝在 MSIX 套件中](/windows/msix/desktop/desktop-to-uwp-root)。</span><span class="sxs-lookup"><span data-stu-id="4a19c-109">Therefore, if an API requires a package identity, a WPF, Windows Forms, or Win32 app cannot call it unless the app [is packaged in an MSIX package](/windows/msix/desktop/desktop-to-uwp-root).</span></span>

## <a name="the-dualapipartition-attribute"></a><span data-ttu-id="4a19c-110">DualApiPartition 屬性</span><span class="sxs-lookup"><span data-stu-id="4a19c-110">The DualApiPartition attribute</span></span>

<span data-ttu-id="4a19c-111">當您想要從桌面應用程式呼叫特定的 WinRT 時，這就是要遵循的流程。</span><span class="sxs-lookup"><span data-stu-id="4a19c-111">This is the process to follow whenever there's a particular WinRT that you'd like to call from your desktop app.</span></span> <span data-ttu-id="4a19c-112">此程式會回答問題，指出是否允許從桌面應用程式呼叫 API。</span><span class="sxs-lookup"><span data-stu-id="4a19c-112">This process will answer the question of whether the API is allowed to be called from a desktop app.</span></span> <span data-ttu-id="4a19c-113">首先，請造訪 [Windows 執行階段 apps 的 WINDOWS API 參考](/uwp/)、找出您感興趣之類別或成員 API 的參考主題，並檢查 [**DualApiPartition**](/uwp/api/Windows.Foundation.Metadata.DualApiPartitionAttribute) 屬性是否列在 [屬性] 區段中。</span><span class="sxs-lookup"><span data-stu-id="4a19c-113">First, visit the [Windows API reference for Windows Runtime apps](/uwp/), find the reference topic for the class or member API you're interested in, and check whether the [**DualApiPartition**](/uwp/api/Windows.Foundation.Metadata.DualApiPartitionAttribute) attribute is listed in the Attributes section.</span></span>

## <a name="if-the-dualapipartition-attribute-is-listed"></a><span data-ttu-id="4a19c-114">如果已列出 DualApiPartition 屬性</span><span class="sxs-lookup"><span data-stu-id="4a19c-114">If the DualApiPartition attribute is listed</span></span>

<span data-ttu-id="4a19c-115">如果列出 DualApiPartition 屬性，則 API 不需要呼叫應用程式具有套件身分識別，且可從任何傳統型應用程式呼叫 API。</span><span class="sxs-lookup"><span data-stu-id="4a19c-115">If the DualApiPartition attribute is listed, the API does not need the calling app to have a package identity, and the API is allowed to be called from any desktop app.</span></span> <span data-ttu-id="4a19c-116">[**Geolocator**](/uwp/api/Windows.Devices.Geolocation.Geolocator) 是一個範例;應用程式不需要唯一識別，即可執行位置工作。</span><span class="sxs-lookup"><span data-stu-id="4a19c-116">[**Windows.Devices.Geolocation.Geolocator**](/uwp/api/Windows.Devices.Geolocation.Geolocator) is an example; an app does not need to be uniquely identified in order to perform location tasks.</span></span>

## <a name="if-the-dualapipartition-attribute-is-not-listed"></a><span data-ttu-id="4a19c-117">如果未列出 DualApiPartition 屬性</span><span class="sxs-lookup"><span data-stu-id="4a19c-117">If the DualApiPartition attribute is not listed</span></span>

<span data-ttu-id="4a19c-118">如果未列出 DualApiPartition 屬性，則 API 會要求呼叫應用程式必須有套件身分識別。</span><span class="sxs-lookup"><span data-stu-id="4a19c-118">If the DualApiPartition attribute is not listed, the API does need the calling app to have a package identity.</span></span> <span data-ttu-id="4a19c-119">因此，除非應用程式已轉換成 UWP 應用程式，否則不允許 WPF、Windows Forms 或 Win32 應用程式呼叫 API。</span><span class="sxs-lookup"><span data-stu-id="4a19c-119">Therefore a WPF, Windows Forms, or Win32 app is not allowed to call the API unless the app has been converted to a UWP app.</span></span> <span data-ttu-id="4a19c-120">例如，您可以使用 [...][**按鈕**](/uwp/api/Windows.UI.Xaml.Controls.Button)。</span><span class="sxs-lookup"><span data-stu-id="4a19c-120">[**Windows.UI.Xaml.Controls.Button**](/uwp/api/Windows.UI.Xaml.Controls.Button) is an example.</span></span>
