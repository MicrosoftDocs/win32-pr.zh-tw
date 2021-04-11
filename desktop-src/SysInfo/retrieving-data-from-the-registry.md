---
description: 若要從登錄取出資料，應用程式通常會列舉金鑰的子機碼，直到它找到特定的子機碼，然後從與其相關聯的值取得資料。
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: 從登錄中取出資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8dd6f6e4d667cf2760c7cba441200755fb6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027394"
---
# <a name="retrieving-data-from-the-registry"></a><span data-ttu-id="68ef7-103">從登錄中取出資料</span><span class="sxs-lookup"><span data-stu-id="68ef7-103">Retrieving Data from the Registry</span></span>

<span data-ttu-id="68ef7-104">若要從登錄取出資料，應用程式通常會列舉金鑰的子機碼，直到它找到特定的子機碼，然後從與其相關聯的值取得資料。</span><span class="sxs-lookup"><span data-stu-id="68ef7-104">To retrieve data from the registry, an application typically enumerates the subkeys of a key until it finds a particular one and then retrieves data from the value or values associated with it.</span></span> <span data-ttu-id="68ef7-105">應用程式可以呼叫 [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) 函式來列舉指定機碼的子機碼。</span><span class="sxs-lookup"><span data-stu-id="68ef7-105">An application can call the [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) function to enumerate the subkeys of a given key.</span></span>

<span data-ttu-id="68ef7-106">若要取得特定子機碼的詳細資料，應用程式可以呼叫 [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) 函數。</span><span class="sxs-lookup"><span data-stu-id="68ef7-106">To retrieve detailed data about a particular subkey, an application can call the [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) function.</span></span> <span data-ttu-id="68ef7-107">[**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)函式會捕獲保護金鑰的安全描述項複本。</span><span class="sxs-lookup"><span data-stu-id="68ef7-107">The [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) function retrieves a copy of the security descriptor protecting a key.</span></span>

<span data-ttu-id="68ef7-108">應用程式可以使用 [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) 函式來列舉指定索引鍵的值，並使用 [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) 函式來取得索引鍵的特定值。</span><span class="sxs-lookup"><span data-stu-id="68ef7-108">An application can use the [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) function to enumerate the values for a given key, and [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) function to retrieve a particular value for a key.</span></span> <span data-ttu-id="68ef7-109">應用程式通常會呼叫 **RegEnumValue** 來判斷值名稱，然後 **RegQueryValueEx** 來取得名稱的資料。</span><span class="sxs-lookup"><span data-stu-id="68ef7-109">An application typically calls **RegEnumValue** to determine the value names and then **RegQueryValueEx** to retrieve the data for the names.</span></span>

<span data-ttu-id="68ef7-110">[**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)函式會抓取與開啟登錄機碼相關聯之值名稱清單的類型和資料。</span><span class="sxs-lookup"><span data-stu-id="68ef7-110">The [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) function retrieves the type and data for a list of value names associated with an open registry key.</span></span> <span data-ttu-id="68ef7-111">此函數對動態金鑰提供者很有用，因為它會在不可部分完成的作業中抓取多個值，以確保資料的一致性。</span><span class="sxs-lookup"><span data-stu-id="68ef7-111">This function is useful for dynamic key providers because it assures consistency of data by retrieving multiple values in an atomic operation.</span></span>

<span data-ttu-id="68ef7-112">由於其他應用程式可以在您的應用程式可以讀取值和使用它的時間之間變更登錄值中的資料，因此您可能需要確定您的應用程式具有最新的資料。</span><span class="sxs-lookup"><span data-stu-id="68ef7-112">Because other applications can change the data in a registry value between the time your application can read a value and use it, you may need to ensure your application has the latest data.</span></span> <span data-ttu-id="68ef7-113">當登錄機碼的屬性或內容有所變更，或刪除金鑰時，您可以使用 [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) 函式來通知呼叫的執行緒。</span><span class="sxs-lookup"><span data-stu-id="68ef7-113">You can use the [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) function to notify the calling thread when there are changes to the attributes or contents of a registry key, or if the key is deleted.</span></span> <span data-ttu-id="68ef7-114">此函式會通知事件物件以通知呼叫者。</span><span class="sxs-lookup"><span data-stu-id="68ef7-114">The function signals an event object to notify the caller.</span></span> <span data-ttu-id="68ef7-115">如果呼叫 **RegNotifyChangeKeyValue** 的執行緒結束，則會將事件發出信號，並停止監視登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="68ef7-115">If the thread that calls **RegNotifyChangeKeyValue** exits, the event is signaled and the monitoring of the registry key is stopped.</span></span>

<span data-ttu-id="68ef7-116">您可以透過使用通知篩選或旗標來控制或指定應該報告的變更。</span><span class="sxs-lookup"><span data-stu-id="68ef7-116">You can control or specify what changes should be reported through the use of a notify filter or flag.</span></span> <span data-ttu-id="68ef7-117">通常，藉由對您指定給函式的事件發出信號來回報變更。</span><span class="sxs-lookup"><span data-stu-id="68ef7-117">Usually, changes are reported by signaling an event that you specify to the function.</span></span> <span data-ttu-id="68ef7-118">請注意， [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) 函式無法用於遠端控制碼。</span><span class="sxs-lookup"><span data-stu-id="68ef7-118">Note that the [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) function does not work with remote handles.</span></span>

<span data-ttu-id="68ef7-119">若要更詳細地監視登錄作業，請參閱 [**registry**](/windows/desktop/ETW/registry)。</span><span class="sxs-lookup"><span data-stu-id="68ef7-119">To monitor registry operations in more detail, see [**Registry**](/windows/desktop/ETW/registry).</span></span>

 

 
