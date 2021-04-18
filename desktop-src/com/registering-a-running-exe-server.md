---
title: 註冊正在執行的 EXE 伺服器
description: 註冊正在執行的 EXE 伺服器
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301671"
---
# <a name="registering-a-running-exe-server"></a><span data-ttu-id="c96aa-103">註冊正在執行的 EXE 伺服器</span><span class="sxs-lookup"><span data-stu-id="c96aa-103">Registering a Running EXE Server</span></span>

<span data-ttu-id="c96aa-104">啟動可執行檔 (EXE) server 時，它應該呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)，它會在與執行中的物件資料表) 不同的資料表 (不同的資料表中，註冊伺服器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="c96aa-104">When an executable (EXE) server is launched, it should call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), which registers the CLSID for the server in what is called the class table (a different table than the running object table).</span></span> <span data-ttu-id="c96aa-105">當伺服器在類別資料表中註冊時，它會允許服務控制管理員 (SCM) 判斷不需要重新開機類別，因為伺服器已經在執行中。</span><span class="sxs-lookup"><span data-stu-id="c96aa-105">When a server is registered in the class table, it allows the service control manager (SCM) to determine that it is not necessary to launch the class again, because the server is already running.</span></span> <span data-ttu-id="c96aa-106">只有在伺服器未列于類別表中時，SCM 才能檢查登錄是否有適當的值，並啟動與指定 CLSID 相關聯的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c96aa-106">Only if the server is not listed in the class table will the SCM check the registry for appropriate values and launch the server associated with the given CLSID.</span></span>

<span data-ttu-id="c96aa-107">您會將類別的 CLSID 和其 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面的指標傳遞給 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) 。</span><span class="sxs-lookup"><span data-stu-id="c96aa-107">You pass [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) the CLSID for the class and a pointer to its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c96aa-108">後續使用此 CLSID 來呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 的用戶端，將會取得其所要求介面的指標，只要安全性不會禁止它即可。</span><span class="sxs-lookup"><span data-stu-id="c96aa-108">Clients who subsequently call [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with this CLSID will retrieve a pointer to their requested interface, as long as security does not forbid it.</span></span> <span data-ttu-id="c96aa-109"> (請參閱 [實例建立](instance-creation-helper-functions.md) 協助程式函數，以取得數個實例建立和啟用函式的描述。 ) </span><span class="sxs-lookup"><span data-stu-id="c96aa-109">(See [Instance Creation Helper Functions](instance-creation-helper-functions.md) for a description of several instance creation and activation functions.)</span></span>

<span data-ttu-id="c96aa-110">當下列所有條件都成立時，類別物件的伺服器應該呼叫 [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) 來撤銷類別物件 (移除其註冊) ：</span><span class="sxs-lookup"><span data-stu-id="c96aa-110">The server for a class object should call [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) to revoke the class object (remove its registration) when all of the following are true:</span></span>

-   <span data-ttu-id="c96aa-111">沒有物件定義的現有實例。</span><span class="sxs-lookup"><span data-stu-id="c96aa-111">There are no existing instances of the object definition.</span></span>
-   <span data-ttu-id="c96aa-112">類別物件上沒有鎖定。</span><span class="sxs-lookup"><span data-stu-id="c96aa-112">There are no locks on the class object.</span></span>
-   <span data-ttu-id="c96aa-113">提供服務給類別物件的應用程式不在使用者控制項下， (顯示) 的使用者看不到。</span><span class="sxs-lookup"><span data-stu-id="c96aa-113">The application providing services to the class object is not under user control (not visible to the user on the display).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c96aa-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="c96aa-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c96aa-115">安裝為服務應用程式</span><span class="sxs-lookup"><span data-stu-id="c96aa-115">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="c96aa-116">在安裝時註冊類別</span><span class="sxs-lookup"><span data-stu-id="c96aa-116">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="c96aa-117">在 ROT 中註冊物件</span><span class="sxs-lookup"><span data-stu-id="c96aa-117">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="c96aa-118">自我註冊</span><span class="sxs-lookup"><span data-stu-id="c96aa-118">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 




