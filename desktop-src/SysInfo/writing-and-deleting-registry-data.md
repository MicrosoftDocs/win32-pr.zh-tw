---
description: 應用程式可以使用 RegSetValueEx 函式，將值和其資料與索引鍵建立關聯。 如需 RegSetValueEx 所支援之實數值型別的清單，請參閱登錄數值型別。
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: 寫入和刪除登錄資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318988"
---
# <a name="writing-and-deleting-registry-data"></a><span data-ttu-id="b298d-104">寫入和刪除登錄資料</span><span class="sxs-lookup"><span data-stu-id="b298d-104">Writing and Deleting Registry Data</span></span>

<span data-ttu-id="b298d-105">應用程式可以使用 [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) 函式，將值和其資料與索引鍵建立關聯。</span><span class="sxs-lookup"><span data-stu-id="b298d-105">An application can use the [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) function to associate a value and its data with a key.</span></span> <span data-ttu-id="b298d-106">如需 **RegSetValueEx** 所支援之實數值型別的清單，請參閱登錄 [數值型別](registry-value-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b298d-106">For a list of the value types supported by **RegSetValueEx**, see [Registry Value Types](registry-value-types.md).</span></span>

<span data-ttu-id="b298d-107">若要從索引鍵刪除值，應用程式可以使用 [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) 函數。</span><span class="sxs-lookup"><span data-stu-id="b298d-107">To delete a value from a key, an application can use the [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) function.</span></span> <span data-ttu-id="b298d-108">若要刪除索引鍵，可以使用 [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) 函數。</span><span class="sxs-lookup"><span data-stu-id="b298d-108">To delete a key, it can use the [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) function.</span></span> <span data-ttu-id="b298d-109">刪除的金鑰必須等到最後一個控制碼關閉後才會移除。</span><span class="sxs-lookup"><span data-stu-id="b298d-109">A deleted key is not removed until the last handle to it has been closed.</span></span> <span data-ttu-id="b298d-110">無法在已刪除的金鑰下建立子機碼和值。</span><span class="sxs-lookup"><span data-stu-id="b298d-110">Subkeys and values cannot be created under a deleted key.</span></span>

<span data-ttu-id="b298d-111">您無法在寫入作業期間鎖定登錄機碼，以同步處理資料的存取。</span><span class="sxs-lookup"><span data-stu-id="b298d-111">It is not possible to lock a registry key during a write operation to synchronize access to the data.</span></span> <span data-ttu-id="b298d-112">不過，您可以使用安全性屬性來控制登錄機碼的存取。</span><span class="sxs-lookup"><span data-stu-id="b298d-112">However, you can control access to a registry key using security attributes.</span></span> <span data-ttu-id="b298d-113">如需詳細資訊，請參閱登錄機 [碼安全性和存取權限](registry-key-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="b298d-113">For more information, see [Registry Key Security and Access Rights](registry-key-security-and-access-rights.md).</span></span>

<span data-ttu-id="b298d-114">您可以在單一交易內執行多個登錄作業。</span><span class="sxs-lookup"><span data-stu-id="b298d-114">More than one registry operation can be performed within a single transaction.</span></span> <span data-ttu-id="b298d-115">若要建立登錄機碼與交易的關聯，應用程式可以使用 [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) 或 [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) 函數。</span><span class="sxs-lookup"><span data-stu-id="b298d-115">To associate a registry key with a transaction, an application can use the [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) or [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) function.</span></span> <span data-ttu-id="b298d-116">如需交易的詳細資訊，請參閱 [核心交易管理員](/windows/desktop/Ktm/kernel-transaction-manager-portal)。</span><span class="sxs-lookup"><span data-stu-id="b298d-116">For more information about transactions, see [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).</span></span>

 

 
