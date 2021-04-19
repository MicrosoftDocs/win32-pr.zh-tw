---
description: 存取 COM + 類別目錄
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: 存取 COM + 類別目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de7c87da1744e23b384199dce68628fd77d5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973973"
---
# <a name="accessing-the-com-catalog"></a><span data-ttu-id="39a18-103">存取 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="39a18-103">Accessing the COM+ Catalog</span></span>

<span data-ttu-id="39a18-104">COM + 類別目錄是保存所有 COM + 設定資料的基礎資料存放區。</span><span class="sxs-lookup"><span data-stu-id="39a18-104">The COM+ catalog is the underlying data store that holds all COM+ configuration data.</span></span> <span data-ttu-id="39a18-105">當您進行任何類型的 COM + 管理時，您會讀取和寫入儲存在目錄中的資料。</span><span class="sxs-lookup"><span data-stu-id="39a18-105">Whenever you do any kind of COM+ administration, you are reading and writing data stored in the catalog.</span></span> <span data-ttu-id="39a18-106">您可以存取類別目錄的唯一方法是透過 [元件服務] 系統管理工具，或透過 COMAdmin 程式庫。</span><span class="sxs-lookup"><span data-stu-id="39a18-106">The only way that you can access the catalog is through the Component Services administrative tool or through the COMAdmin library.</span></span>

<span data-ttu-id="39a18-107">COM + 類別目錄提供抽象層，可瞭解如何儲存 COM + 設定資料的實際詳細資料。</span><span class="sxs-lookup"><span data-stu-id="39a18-107">The COM+ catalog provides a layer of abstraction over the actual details of where and how COM+ configuration data is stored.</span></span> <span data-ttu-id="39a18-108">大部分的資料都儲存在 COM + 註冊資料庫 (或 RegDB) ，其中包含安裝在 COM + 應用程式中所有已設定元件的資料。</span><span class="sxs-lookup"><span data-stu-id="39a18-108">Much of the data is stored in the COM+ registration database (or RegDB), which holds data for all configured components installed in COM+ applications.</span></span> <span data-ttu-id="39a18-109">此資料庫會在應用程式執行時間使用，以將設定資料提供給 COM +，以便在適當的內容中適當地啟用物件，並根據其設定為物件提供服務。</span><span class="sxs-lookup"><span data-stu-id="39a18-109">This database is used at application run time to provide configuration data to COM+ to properly activate objects in an appropriate context, enabling services to be provided for objects per their configuration.</span></span> <span data-ttu-id="39a18-110">RegDB 本身是一種交易式資源管理員，可透過 [補償資源管理員](com--compensating-resource-manager.md)使用 DTC 交易;當您進行保存的設定變更時，它們會以交易方式認可。</span><span class="sxs-lookup"><span data-stu-id="39a18-110">The RegDB itself is a transacted resource manager that uses DTC transactions through the [compensating resource manager](com--compensating-resource-manager.md); when you make persisted configuration changes, they are committed transactionally.</span></span> <span data-ttu-id="39a18-111">存取 RegDB 的唯一方法是使用 COMAdmin 物件或元件服務系統管理工具，透過 COM + 類別目錄來存取。</span><span class="sxs-lookup"><span data-stu-id="39a18-111">The only way that you can access the RegDB is through the COM+ catalog, using the COMAdmin objects or the Component Services administrative tool.</span></span>

<span data-ttu-id="39a18-112">在每部電腦上，都有一個在系統應用程式中以元件的形式執行的 COM + 類別目錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="39a18-112">On each computer, there is a COM+ catalog server running as a component in the system application.</span></span> <span data-ttu-id="39a18-113">目錄伺服器可控制存取儲存在其電腦上的目錄資料。實際上，目錄伺服器是一種查詢引擎，可讓您在該電腦的目錄中讀取和寫入資料。</span><span class="sxs-lookup"><span data-stu-id="39a18-113">The catalog server controls access to the catalog data stored on its machine; in effect, the catalog server is a query engine that allows you to read and write data in the catalog on that machine.</span></span> <span data-ttu-id="39a18-114">當您透過具現化 [**COMAdminCatalog**](comadmincatalog.md) 物件來起始程式設計管理時，此物件會開啟本機目錄伺服器的會話。</span><span class="sxs-lookup"><span data-stu-id="39a18-114">When you initiate programmatic administration by instantiating a [**COMAdminCatalog**](comadmincatalog.md) object, this object opens a session with the local catalog server.</span></span> <span data-ttu-id="39a18-115">本機目錄伺服器會處理本機目錄上集合或集合專案的要求。</span><span class="sxs-lookup"><span data-stu-id="39a18-115">Requests for collections or collection items on the local catalog are handled by the local catalog server.</span></span> <span data-ttu-id="39a18-116">當您連線到遠端電腦時，您會與該電腦上的目錄伺服器進行通訊。</span><span class="sxs-lookup"><span data-stu-id="39a18-116">When you connect to a remote machine, you are communicating with the catalog server on that machine.</span></span>

## <a name="security-considerations-in-administration"></a><span data-ttu-id="39a18-117">管理中的安全性考慮</span><span class="sxs-lookup"><span data-stu-id="39a18-117">Security Considerations in Administration</span></span>

<span data-ttu-id="39a18-118">若要變更 COM + 類別目錄上的資料，您必須以系統管理員的身分擁有授權單位。</span><span class="sxs-lookup"><span data-stu-id="39a18-118">To change data on the COM+ catalog, you need to have authority as an administrator.</span></span> <span data-ttu-id="39a18-119">若要使用 [元件服務] 系統管理工具來變更任何設定資料，您必須是系統管理員角色的成員，且該角色已指派給您嘗試管理的電腦上的系統應用程式。</span><span class="sxs-lookup"><span data-stu-id="39a18-119">To use the Component Services administrative tool to change any configuration data, you need to be a member of the Administrators role assigned to the system application on the machine you are trying to administer.</span></span> <span data-ttu-id="39a18-120">同樣地，若要使用 COMAdmin 物件變更任何資料，您的程式碼必須以系統管理員授權單位執行。</span><span class="sxs-lookup"><span data-stu-id="39a18-120">Likewise, to change any data by using the COMAdmin objects, your code needs to be running with Administrator authority.</span></span> <span data-ttu-id="39a18-121">也就是說，使用 COMAdmin 物件的應用程式或腳本，必須在其嘗試管理的電腦上，于系統應用程式上指派為系統管理員角色的使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="39a18-121">That is, an application or script using the COMAdmin objects must be running under a user account that is assigned to the Administrators role on the system application on the machine that it is trying to administer.</span></span> <span data-ttu-id="39a18-122">應用程式只能存取類別目錄上的資訊，並將其變更為其執行所在之帳戶所屬的範圍。</span><span class="sxs-lookup"><span data-stu-id="39a18-122">The application can access and change information on the catalog only to the extent that the account under which it is running has that authority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39a18-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="39a18-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39a18-124">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="39a18-124">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="39a18-125">COMAdmin 類別的摘要描述</span><span class="sxs-lookup"><span data-stu-id="39a18-125">Summary Description of the COMAdmin Classes</span></span>](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



