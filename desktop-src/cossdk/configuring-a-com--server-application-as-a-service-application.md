---
description: 您可以將 COM + 伺服器應用程式建立為服務，以在系統啟動期間自動啟動，或在啟動時以手動方式啟動。
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: 將 COM + 伺服器應用程式設定為服務應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847158"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a><span data-ttu-id="e6272-103">將 COM + 伺服器應用程式設定為服務應用程式</span><span class="sxs-lookup"><span data-stu-id="e6272-103">Configuring a COM+ Server Application as a Service Application</span></span>

<span data-ttu-id="e6272-104">您可以將 COM + 伺服器應用程式建立為服務，以在系統啟動期間自動啟動，或在啟動時以手動方式啟動。</span><span class="sxs-lookup"><span data-stu-id="e6272-104">A COM+ server application can be created as a service to start either automatically during the system startup or manually by activations.</span></span> <span data-ttu-id="e6272-105">如果服務無法啟動，則錯誤處理的選項會指定錯誤的嚴重性，並決定要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="e6272-105">If the service fails to start, the option for error handling specifies the severity of the error and determines the action to be taken.</span></span> <span data-ttu-id="e6272-106">也可以使用將服務設定為 [本機系統] 帳戶執行的選項，以及指派要執行 COM + 伺服器應用程式之特定使用者帳戶的選項。</span><span class="sxs-lookup"><span data-stu-id="e6272-106">The option to configure a service to run as the local system account is also available, as well as the option to assign a specific user account for which the COM+ server application will run.</span></span> <span data-ttu-id="e6272-107">也可以使用 [元件服務]，從電腦上註冊的服務清單中選取相依性。</span><span class="sxs-lookup"><span data-stu-id="e6272-107">Dependencies can also be selected from a list of services registered on the computer using Component Services.</span></span> <span data-ttu-id="e6272-108">這會決定在此服務啟動之前必須執行的服務。</span><span class="sxs-lookup"><span data-stu-id="e6272-108">This will determine which services must be executed before this service is started.</span></span>

<span data-ttu-id="e6272-109">**將 COM + 應用程式設定為以服務方式執行**</span><span class="sxs-lookup"><span data-stu-id="e6272-109">**To configure a COM+ application to run as a service**</span></span>

1.  <span data-ttu-id="e6272-110">在 [元件服務] 系統管理工具的主控台樹中，找出您想要以服務方式執行的 COM + 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="e6272-110">In the console tree of the Component Services administrative tool, locate the COM+ server application you want to run as a service.</span></span>

2.  <span data-ttu-id="e6272-111">以滑鼠右鍵按一下 COM + 伺服器應用程式，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="e6272-111">Right-click the COM+ server application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="e6272-112">在 [ **屬性** ] 對話方塊中，按一下 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="e6272-112">In the **Properties** dialog box, click the **Activation** tab.</span></span>

4.  <span data-ttu-id="e6272-113">在 [ **啟用類型** ] 方塊中，核取 [以 **NT 服務的形式執行應用程式** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="e6272-113">In the **Activation type** box, check the **Run application as NT Service** check box.</span></span>

    > [!Note]  
    > <span data-ttu-id="e6272-114">[以 **NT 服務的形式執行應用程式** ] 核取方塊只會針對伺服器應用程式啟用，而且會針對程式庫應用程式停用。</span><span class="sxs-lookup"><span data-stu-id="e6272-114">The **Run application as NT Service** check box is enabled only for server applications and is disabled for library applications.</span></span>

     

5.  <span data-ttu-id="e6272-115">按一下 [ **設定新服務** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="e6272-115">Click the **Setup New Service** button.</span></span>

6.  <span data-ttu-id="e6272-116">在 [**服務名稱**] 對話方塊的 [**啟動類型**] 方塊中，選取 [**自動**] 或 [**手動**]。</span><span class="sxs-lookup"><span data-stu-id="e6272-116">In the **Startup type** box in the **Service Name** dialog box, select **Automatic** or **Manual**.</span></span>

7.  <span data-ttu-id="e6272-117"> (選擇性) 指定要針對特定錯誤採取的動作，請在 [**錯誤處理**] 方塊中選取 [**忽略**]、[**正常**]、[**嚴重**] 或 [**重大**]。</span><span class="sxs-lookup"><span data-stu-id="e6272-117">(Optional) To specify the action to be taken for a particular error, select **Ignore**, **Normal**, **Severe**, or **Critical** in the **Error Handling** box.</span></span> <span data-ttu-id="e6272-118">與每個選項相關聯的行為如下所示：</span><span class="sxs-lookup"><span data-stu-id="e6272-118">The behavior associated with each option is as follows:</span></span>

    1.  <span data-ttu-id="e6272-119">**Ignore**。</span><span class="sxs-lookup"><span data-stu-id="e6272-119">**Ignore**.</span></span> <span data-ttu-id="e6272-120">啟動程式會記錄錯誤，但會繼續執行啟動操作。</span><span class="sxs-lookup"><span data-stu-id="e6272-120">The startup program logs the error but continues the startup operation.</span></span>
    2.  <span data-ttu-id="e6272-121">**正常**。</span><span class="sxs-lookup"><span data-stu-id="e6272-121">**Normal**.</span></span> <span data-ttu-id="e6272-122">會記錄錯誤、顯示訊息方塊，且啟動程式會繼續執行啟動作業。</span><span class="sxs-lookup"><span data-stu-id="e6272-122">The error is logged, a message box is displayed, and the startup program continues the startup operation.</span></span>
    3.  <span data-ttu-id="e6272-123">**嚴重**。</span><span class="sxs-lookup"><span data-stu-id="e6272-123">**Severe**.</span></span> <span data-ttu-id="e6272-124">系統會記錄錯誤，並以最後一個已知的正確設定重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="e6272-124">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="e6272-125">如果這是記錄錯誤時正在啟動的最後一個已知正確設定，則會繼續執行啟動作業。</span><span class="sxs-lookup"><span data-stu-id="e6272-125">If it is the last known good configuration that is being started when the error is logged, the startup operation continues.</span></span>
    4.  <span data-ttu-id="e6272-126">**重大**：</span><span class="sxs-lookup"><span data-stu-id="e6272-126">**Critical**.</span></span> <span data-ttu-id="e6272-127">系統會記錄錯誤，並以最後一個已知的正確設定重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="e6272-127">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="e6272-128">如果這是記錄錯誤時正在啟動的最後一個已知正確設定，則啟動作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="e6272-128">If it is the last known good configuration that is being started when the error is logged, the startup operation fails.</span></span>

8.  <span data-ttu-id="e6272-129"> (選擇性的) 若要將其他服務設定為相依，請從 [相依性 **]** 方塊中的清單選取相依的服務。</span><span class="sxs-lookup"><span data-stu-id="e6272-129">(Optional) To set other services as dependent, select the dependent services from the list in the **Dependencies** box.</span></span>

9.  <span data-ttu-id="e6272-130"> (選擇性的) 表示應該允許服務與桌面互動，請勾選 [ **允許服務與桌面互動]** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="e6272-130">(Optional) To indicate that the service should be allowed to interact with the desktop, check the **Allow service to interact with desktop** check box.</span></span>

10. <span data-ttu-id="e6272-131">按一下頁面底部的 [新增]  。</span><span class="sxs-lookup"><span data-stu-id="e6272-131">Click **Create**.</span></span>

11. <span data-ttu-id="e6272-132"> (選擇性) 將服務指派給使用者帳戶：</span><span class="sxs-lookup"><span data-stu-id="e6272-132">(Optional) To assign the service to a user account:</span></span>

    1.  <span data-ttu-id="e6272-133">在 [身分 **識別** ] 索引標籤中，選取 [ **此使用者**]。</span><span class="sxs-lookup"><span data-stu-id="e6272-133">In the **Identity** tab, select **This user**.</span></span>
    2.  <span data-ttu-id="e6272-134">若要選取使用者，請在 [ **使用者** ] 方塊中輸入使用者名稱，或按一下 [ **流覽]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="e6272-134">To select the user, enter the user name in the **User** box or click the **Browse** button.</span></span>
    3.  <span data-ttu-id="e6272-135">在 [ **密碼** ] 方塊中輸入使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="e6272-135">Enter the password for the user account in the **Password** box.</span></span>
    4.  <span data-ttu-id="e6272-136">在 [ **確認密碼** ] 方塊中輸入相同的密碼。</span><span class="sxs-lookup"><span data-stu-id="e6272-136">Enter the same password in the **Confirm Password** box.</span></span>

 

 



