---
title: 裝置存取 API
description: 使用裝置存取 API 來撰寫使用自訂驅動程式之特製化裝置的 Windows Store 裝置應用程式。
ms.assetid: 51329746-291e-4ac6-9029-ebe4727d5d7d
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 6f054167d81f33ce852f7707e194058f4cee3c75
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383190"
---
# <a name="device-access-api"></a><span data-ttu-id="e1ec2-103">裝置存取 API</span><span class="sxs-lookup"><span data-stu-id="e1ec2-103">Device Access API</span></span>

## <a name="purpose"></a><span data-ttu-id="e1ec2-104">目的</span><span class="sxs-lookup"><span data-stu-id="e1ec2-104">Purpose</span></span>

<span data-ttu-id="e1ec2-105">您可以使用裝置存取 API 來撰寫使用自訂驅動程式之特製化裝置的 Windows Store 裝置應用程式。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-105">You can use the Device Access API to write Windows Store device apps for specialized devices that use custom drivers.</span></span> <span data-ttu-id="e1ec2-106">API 會提供方法來傳送控制程式代碼，以與裝置的自訂驅動程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-106">The API provides methods for sending control codes to communicate with the device's custom driver.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e1ec2-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="e1ec2-107">In this section</span></span>

| <span data-ttu-id="e1ec2-108">主題</span><span class="sxs-lookup"><span data-stu-id="e1ec2-108">Topic</span></span> | <span data-ttu-id="e1ec2-109">描述</span><span class="sxs-lookup"><span data-stu-id="e1ec2-109">Description</span></span> |
|---|---|
| [<span data-ttu-id="e1ec2-110">關於裝置存取 API</span><span class="sxs-lookup"><span data-stu-id="e1ec2-110">About the Device Access API</span></span>](about-the-device-access-api.md)<br/> | <span data-ttu-id="e1ec2-111">裝置存取 API 適用于建立 Windows Store 應用程式的 c + + 開發人員，以便與 Windows 8 中的特殊裝置互動。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-111">The Device Access API is for C++ developers who are creating a Windows Store app to interact with specialized devices in Windows 8.</span></span> <span data-ttu-id="e1ec2-112">本主題說明裝置存取 API 適用的案例。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-112">This topic describes the scenarios that the Device Access API applies to.</span></span> <span data-ttu-id="e1ec2-113">此外，也會說明裝置存取 API 如何在 Windows 8 中套用 Windows Store 應用程式的安全性規則。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-113">It also explains how the Device Access API applies security rules for Windows Store apps in Windows 8.</span></span><br/> |
| [<span data-ttu-id="e1ec2-114">如何使用裝置存取 API</span><span class="sxs-lookup"><span data-stu-id="e1ec2-114">How to Use the Device Access API</span></span>](using-the-device-access-api.md)<br/> | <span data-ttu-id="e1ec2-115">本主題包含使用裝置存取 API 的工作和設計考慮。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-115">This topic contains tasks and design considerations for using the Device Access API.</span></span><br/> |
| [<span data-ttu-id="e1ec2-116">裝置存取 API c + + 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="e1ec2-116">Device Access API C++ Programming Reference</span></span>](device-access-api-c---programming-reference.md)<br/> | <span data-ttu-id="e1ec2-117">提供裝置存取 API 中函數和介面的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-117">Provides reference pages for the functions and interfaces in the Device Access API.</span></span><br/> |
| [<span data-ttu-id="e1ec2-118">裝置存取詞彙</span><span class="sxs-lookup"><span data-stu-id="e1ec2-118">Device Access Glossary</span></span>](deviceaccess-glossary.md)<br/> | <span data-ttu-id="e1ec2-119">以下是在裝置存取 API 的檔中使用的詞彙。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-119">The following are terms used throughout the documentation for the Device Access API.</span></span><br/> |
| [<span data-ttu-id="e1ec2-120">其他 API</span><span class="sxs-lookup"><span data-stu-id="e1ec2-120">Other APIs</span></span>](other-apis.md)<br/> | <span data-ttu-id="e1ec2-121">這些介面不受支援，且不應該使用。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-121">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="e1ec2-122">請改用 [裝置存取 API c + + 程式設計參考](device-access-api-c---programming-reference.md) 中的 api。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-122">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="e1ec2-123">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e1ec2-123">Developer audience</span></span>

<span data-ttu-id="e1ec2-124">裝置存取 API 是專為獨立硬體廠商 (IHV) 以及熟悉 c + + 和元件物件模型 (COM) 的 OEM 開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="e1ec2-124">The Device Access API is designed for independent hardware vendor (IHV) and OEM developers who are familiar with C++ and Component Object Model (COM).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1ec2-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1ec2-125">Related topics</span></span>

<span data-ttu-id="e1ec2-126">[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、 [硬體開發人員中心](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="e1ec2-126">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
