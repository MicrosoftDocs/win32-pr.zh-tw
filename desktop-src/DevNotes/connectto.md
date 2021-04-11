---
description: HKLM \\ SOFTWARE \\ Microsoft \\ MSSQLServer \\ Client。
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025893"
---
# <a name="connectto"></a><span data-ttu-id="5490a-103">ConnectTo</span><span class="sxs-lookup"><span data-stu-id="5490a-103">ConnectTo</span></span>

<span data-ttu-id="5490a-104">**HKLM \\ SOFTWARE \\ Microsoft \\ MSSQLServer \\ 用戶端**</span><span class="sxs-lookup"><span data-stu-id="5490a-104">**HKLM\\SOFTWARE\\Microsoft\\MSSQLServer\\Client**</span></span>

## <a name="description"></a><span data-ttu-id="5490a-105">Description</span><span class="sxs-lookup"><span data-stu-id="5490a-105">Description</span></span>

<span data-ttu-id="5490a-106">**ConnectTo** 子機碼會儲存連接至 Microsoft SQL Server database engine 實例之以 Windows 為基礎的用戶端的連接資訊。</span><span class="sxs-lookup"><span data-stu-id="5490a-106">The **ConnectTo** subkey stores connection information for Windows-based clients that connect to instances of the Microsoft SQL Server database engine.</span></span> <span data-ttu-id="5490a-107">此子機碼中的登錄專案屬於資料類型 REG \_ SZ，而其值會指定要用來連接到實例的 Net-Library，以及任何網路特定的參數。</span><span class="sxs-lookup"><span data-stu-id="5490a-107">Registry entries in this subkey are of data type REG\_SZ, and their values specify the Net-Library to use for connecting to the instance, as well as any network-specific parameters.</span></span>

<span data-ttu-id="5490a-108">此子機碼中儲存的連接資訊是由 SQL Server、SQL Server ODBC 驅動程式或 SQL Server DB-Library 動態連結程式庫 (DLL) 的 OLE DB 提供者讀取。</span><span class="sxs-lookup"><span data-stu-id="5490a-108">The connection information stored in this subkey is read by the OLE DB Provider for SQL Server, the SQL Server ODBC driver, or the SQL Server DB-Library dynamic-link library (DLL).</span></span>

## <a name="change-method"></a><span data-ttu-id="5490a-109">變更方法</span><span class="sxs-lookup"><span data-stu-id="5490a-109">Change Method</span></span>

<span data-ttu-id="5490a-110">您不應該使用 [登錄編輯程式] 來修改此子機碼中的專案。</span><span class="sxs-lookup"><span data-stu-id="5490a-110">You should not modify entries in this subkey by using the registry editor.</span></span> <span data-ttu-id="5490a-111">使用 SQL Server 用戶端網路公用程式來設定伺服器名稱和連接資訊。</span><span class="sxs-lookup"><span data-stu-id="5490a-111">Use the SQL Server Client Network Utility to configure server name and connection information.</span></span> <span data-ttu-id="5490a-112">如需進一步指示，請參閱 SQL Server 用戶端網路公用程式說明。</span><span class="sxs-lookup"><span data-stu-id="5490a-112">See SQL Server Client Network Utility Help for further instructions.</span></span>

## <a name="notes"></a><span data-ttu-id="5490a-113">備註</span><span class="sxs-lookup"><span data-stu-id="5490a-113">Notes</span></span>

-   <span data-ttu-id="5490a-114">OLE DB 提供者會使用 **ConnectTo** 子機碼來 SQL Server、SQL Server ODBC 驅動程式和 SQL SERVER DB-Library DLL。</span><span class="sxs-lookup"><span data-stu-id="5490a-114">The **ConnectTo** subkey is used by the OLE DB Provider for SQL Server, the SQL Server ODBC Driver, and the SQL Server DB-Library DLL.</span></span> <span data-ttu-id="5490a-115">此子機碼中的專案會識別 Net-Library 這些資料存取應用程式開發介面 (API) 元件呼叫的專案。</span><span class="sxs-lookup"><span data-stu-id="5490a-115">Entries in this subkey identify which Net-Library these data access application programming interface (API) components call.</span></span>
-   <span data-ttu-id="5490a-116">Net-Libraries 是保護資料存取 API 元件的 SQL Server 元件，從使用不同的處理序間通訊 (IPC) 方法的詳細資料，到與 SQL Server 資料庫引擎的 instancess 通訊。</span><span class="sxs-lookup"><span data-stu-id="5490a-116">Net-Libraries are SQL Server components that shield the data access API components from the details of using different Interprocess Communication (IPC) methods to communicate with an instancess of the SQL Server database engine.</span></span>
-   <span data-ttu-id="5490a-117">不當更新 **ConnectTo** 子機碼可能會導致應用程式無法順利連接到 SQL Server database engine 的實例。</span><span class="sxs-lookup"><span data-stu-id="5490a-117">Improperly updating the **ConnectTo** subkey might prevent applications from successfully connecting to an instance of the SQL Server database engine.</span></span>

 

 



