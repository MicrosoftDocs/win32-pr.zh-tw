---
title: 設定 ADSI 開發的 Visual C++ 6。0
description: 本主題說明如何在 Visual Studio 中設定 c + +，讓您可以開發 ADSI 應用程式。
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- 設定 ADSI 開發的 c + +
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2350b88402c921d014b0c93756759a1d0f744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020788"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a><span data-ttu-id="d4dc7-104">設定 ADSI 開發的 Visual C++ 6。0</span><span class="sxs-lookup"><span data-stu-id="d4dc7-104">Setting Up Visual C++ 6.0 for ADSI Development</span></span>

<span data-ttu-id="d4dc7-105">Microsoft Visual C++ 6.0 開發系統可以用來開發企業應用程式。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-105">The Microsoft Visual C++ 6.0 development system can be used to develop enterprise applications.</span></span> <span data-ttu-id="d4dc7-106">若要設定您的 Visual C++ 6.0 環境以開發 ADSI 應用程式，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d4dc7-106">To set up your Visual C++ 6.0 environment to develop an ADSI application, perform the following steps:</span></span>

<span data-ttu-id="d4dc7-107">**設定 Microsoft Visual C++ 6.0 開發環境**</span><span class="sxs-lookup"><span data-stu-id="d4dc7-107">**Setting Up the Microsoft Visual C++ 6.0 Development Environment**</span></span>

1.  <span data-ttu-id="d4dc7-108">指向 [包含] 和 [程式庫] 目錄。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-108">Point to the include and library directory.</span></span> <span data-ttu-id="d4dc7-109">選取 [ **工具 \| 選項**]。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-109">Select **Tools \| Options**.</span></span> <span data-ttu-id="d4dc7-110">按一下 [ **目錄** ] 索引標籤，並指定 ADSI 標頭檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-110">Click the **Directory** tab, and specify the path to the ADSI header files.</span></span>
2.  <span data-ttu-id="d4dc7-111">在您的專案中包含 Activeds .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-111">Include the Activeds.h file in your project.</span></span>
3.  <span data-ttu-id="d4dc7-112">將 Activeds .lib 和 Adsiid .lib 檔案新增至專案的連結器輸入。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-112">Add the Activeds.lib and Adsiid.lib files to the linker input for your project.</span></span>
4.  <span data-ttu-id="d4dc7-113">開始使用 ADSI 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="d4dc7-114">登入 Windows 網域。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-114">Log on to a Windows domain.</span></span> <span data-ttu-id="d4dc7-115">您也必須具有在 Active Directory 中修改資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-115">You must also have permission to modify data in Active Directory.</span></span> <span data-ttu-id="d4dc7-116">依預設，系統管理員具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-116">By default, the Administrator has this privilege.</span></span> <span data-ttu-id="d4dc7-117">若要輸入此程式碼範例：</span><span class="sxs-lookup"><span data-stu-id="d4dc7-117">To enter this code example:</span></span>

<span data-ttu-id="d4dc7-118">**範例 Visual C++ 應用程式：在網域中建立使用者**</span><span class="sxs-lookup"><span data-stu-id="d4dc7-118">**A Sample Visual C++ Application: Creating a User in a Domain**</span></span>

1.  <span data-ttu-id="d4dc7-119">啟動 Visual C++ 6.0。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-119">Start Visual C++ 6.0.</span></span>
2.  <span data-ttu-id="d4dc7-120">建立獨立可執行檔專案。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-120">Create a standalone executable project.</span></span> <span data-ttu-id="d4dc7-121">它可以是 MFC、ATL 或主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-121">It can be either an MFC, ATL, or Console Application.</span></span>
3.  <span data-ttu-id="d4dc7-122">遵循先前的步驟來設定您的專案。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-122">Follow the previous steps to set up your project.</span></span>
4.  <span data-ttu-id="d4dc7-123">輸入下列程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-123">Enter the following code example.</span></span> <span data-ttu-id="d4dc7-124">以網域中容器的 ADsPath 取代 "LDAP：//CN = users，DC = fabrikam，DC = com" 字串。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-124">Replace the "LDAP://CN=users,DC=fabrikam,DC=com" string with the ADsPath of a container in your domain.</span></span> <span data-ttu-id="d4dc7-125">您也應該使用網域中唯一的使用者名稱來取代使用者名稱 "jeffsmith"。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-125">You should also replace the user name "jeffsmith" with a user name that is unique in your domain.</span></span>

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  <span data-ttu-id="d4dc7-126">建置並執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-126">Build and run the application.</span></span> <span data-ttu-id="d4dc7-127">若要確認是否已建立使用者，請使用 Active Directory 消費者和電腦管理工具。</span><span class="sxs-lookup"><span data-stu-id="d4dc7-127">To verify that the user has been created, use the Active Directory Users and Computers management tool.</span></span>

 

 




