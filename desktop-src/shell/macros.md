---
description: 本節說明 Windows Shell 公用程式宏。
title: Shell 宏
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 085bca918cfa6ca1441272c3c9181226ef603ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944498"
---
# <a name="shell-macros"></a><span data-ttu-id="84949-103">Shell 宏</span><span class="sxs-lookup"><span data-stu-id="84949-103">Shell Macros</span></span>

<span data-ttu-id="84949-104">本節說明 Windows Shell 公用程式宏。</span><span class="sxs-lookup"><span data-stu-id="84949-104">This section describes the Windows Shell utility macros.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84949-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="84949-105">In this section</span></span>



| <span data-ttu-id="84949-106">主題</span><span class="sxs-lookup"><span data-stu-id="84949-106">Topic</span></span>                                                                  | <span data-ttu-id="84949-107">描述</span><span class="sxs-lookup"><span data-stu-id="84949-107">Description</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84949-108">**定義 \_ PROPERTYKEY**</span><span class="sxs-lookup"><span data-stu-id="84949-108">**DEFINE\_PROPERTYKEY**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | <span data-ttu-id="84949-109">用來封裝格式識別碼 (FMTID) 和屬性識別碼 (PID) 為代表屬性索引鍵的 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) 結構。</span><span class="sxs-lookup"><span data-stu-id="84949-109">Used to pack a format identifier (FMTID) and property identifier (PID) into a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure that represents a property key.</span></span><br/>                                                                                    |
| [<span data-ttu-id="84949-110">**IID \_ PPV 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="84949-110">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | <span data-ttu-id="84949-111">用來取出介面指標，並根據所使用介面指標的類型，自動提供所要求介面的 IID 值。</span><span class="sxs-lookup"><span data-stu-id="84949-111">Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used.</span></span> <span data-ttu-id="84949-112">藉由檢查編譯時期傳遞的數值型別，即可避免常見的編碼錯誤。</span><span class="sxs-lookup"><span data-stu-id="84949-112">This avoids a common coding error by checking the type of the value passed at compile time.</span></span><br/> |
| [<span data-ttu-id="84949-113">**IsEqualPropertyKey**</span><span class="sxs-lookup"><span data-stu-id="84949-113">**IsEqualPropertyKey**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | <span data-ttu-id="84949-114">比較兩個 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) 結構的成員，並傳回兩者是否相等。</span><span class="sxs-lookup"><span data-stu-id="84949-114">Compares the members of two [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structures and returns whether they are equal.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="84949-115">**MAKEDLLVERULL**</span><span class="sxs-lookup"><span data-stu-id="84949-115">**MAKEDLLVERULL**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | <span data-ttu-id="84949-116">用來將 DLL 版本資訊封裝成 ULONGLONG 值。</span><span class="sxs-lookup"><span data-stu-id="84949-116">Used to pack DLL version information into a ULONGLONG value.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="84949-117">**NetAddr \_ DisplayErrorTip**</span><span class="sxs-lookup"><span data-stu-id="84949-117">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | <span data-ttu-id="84949-118">在與網路位址控制項相關聯的氣球提示中顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="84949-118">Displays an error message in the balloon tip associated with the network address control.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="84949-119">**NetAddr \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="84949-119">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | <span data-ttu-id="84949-120">指出網路位址是否符合指定的類型和格式。</span><span class="sxs-lookup"><span data-stu-id="84949-120">Indicates whether a network address conforms to a specified type and format.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="84949-121">**NetAddr \_ GetAllowType**</span><span class="sxs-lookup"><span data-stu-id="84949-121">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | <span data-ttu-id="84949-122">抓取指定的網路位址控制項接受的網路位址類型。</span><span class="sxs-lookup"><span data-stu-id="84949-122">Retrieves the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="84949-123">**NetAddr \_ SetAllowType**</span><span class="sxs-lookup"><span data-stu-id="84949-123">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | <span data-ttu-id="84949-124">設定指定的網路位址控制項接受的網路位址類型。</span><span class="sxs-lookup"><span data-stu-id="84949-124">Sets the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                     |



 

 

 
