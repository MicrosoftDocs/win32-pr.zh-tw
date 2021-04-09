---
title: 偵測架構主機
description: Active Directory Domain Services 具有多宿主更新系統;每個網域控制站都會保存目錄的可寫入複本。
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- 偵測架構主機 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/23/2019
ms.locfileid: "103840935"
---
# <a name="detecting-the-schema-master"></a><span data-ttu-id="57f59-104">偵測架構主機</span><span class="sxs-lookup"><span data-stu-id="57f59-104">Detecting the Schema Master</span></span>

<span data-ttu-id="57f59-105">Active Directory Domain Services 具有多宿主更新系統;每個網域控制站都會保存目錄的可寫入複本。</span><span class="sxs-lookup"><span data-stu-id="57f59-105">Active Directory Domain Services have a multi-master update system; every domain controller holds a writable copy of the directory.</span></span> <span data-ttu-id="57f59-106">架構更新會傳播到屬於相同樹狀目錄或樹系的所有網域。</span><span class="sxs-lookup"><span data-stu-id="57f59-106">Schema updates are propagated to all domains that belong to the same tree or forest.</span></span> <span data-ttu-id="57f59-107">因為難以協調衝突的更新與架構，所以只能在單一伺服器上執行架構更新。</span><span class="sxs-lookup"><span data-stu-id="57f59-107">Because it is difficult to reconcile conflicting updates to the schema, schema updates can only be performed at a single server.</span></span> <span data-ttu-id="57f59-108">具有執行更新許可權的伺服器可能會變更，但在任何指定的時間，只有一部伺服器會有該許可權。</span><span class="sxs-lookup"><span data-stu-id="57f59-108">The server with the right to perform updates can change, but only one server will have that right at any given time.</span></span> <span data-ttu-id="57f59-109">此伺服器稱為架構主機。</span><span class="sxs-lookup"><span data-stu-id="57f59-109">This server is called the schema master.</span></span> <span data-ttu-id="57f59-110">依預設，在企業中安裝的第一個 DC 是架構主機。</span><span class="sxs-lookup"><span data-stu-id="57f59-110">The first DC installed in an enterprise is, by default, the schema master.</span></span>

<span data-ttu-id="57f59-111">架構變更只能在架構主機層級進行。</span><span class="sxs-lookup"><span data-stu-id="57f59-111">Schema changes can only be made at the schema master level.</span></span> <span data-ttu-id="57f59-112">若要偵測哪個 DC 是架構主機，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="57f59-112">To detect which DC is the schema master, perform the following steps.</span></span>

<span data-ttu-id="57f59-113">**偵測 DC 架構主機**</span><span class="sxs-lookup"><span data-stu-id="57f59-113">**Detecting the DC Schema Master**</span></span>

1.  <span data-ttu-id="57f59-114">讀取任何 DC 上架構容器的 **fsmoRoleOwner** 屬性。</span><span class="sxs-lookup"><span data-stu-id="57f59-114">Read the **fsmoRoleOwner** attribute of the schema container on any DC.</span></span> <span data-ttu-id="57f59-115">**FsmoRoleOwner** 屬性會傳回架構主機之 **NTDSDSA** 物件 (DN) 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="57f59-115">The **fsmoRoleOwner** attribute returns the distinguished name (DN) of the **nTDSDSA** object for the schema master.</span></span>
2.  <span data-ttu-id="57f59-116">系結至您剛剛抓取其 DN 的 **nTDSDSA** 物件。</span><span class="sxs-lookup"><span data-stu-id="57f59-116">Bind to the **nTDSDSA** object whose DN you just retrieved.</span></span> <span data-ttu-id="57f59-117">此物件的父系是包含架構主機之 DC 的伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="57f59-117">The parent of this object is the server object for the DC containing the schema master.</span></span>
3.  <span data-ttu-id="57f59-118">取得 **nTDSDSA** 物件父系的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="57f59-118">Get the ADsPath for the parent of the **nTDSDSA** object.</span></span> <span data-ttu-id="57f59-119">父系是伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="57f59-119">The parent is a server object.</span></span>
4.  <span data-ttu-id="57f59-120">系結至伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="57f59-120">Bind to the server object.</span></span>
5.  <span data-ttu-id="57f59-121">取得伺服器物件的 **dNSHostName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="57f59-121">Get the **dNSHostName** attribute of the server object.</span></span> <span data-ttu-id="57f59-122">這是包含架構主機之 DC 的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="57f59-122">This is the DNS name of the DC that contains the schema master.</span></span>
6.  <span data-ttu-id="57f59-123">將架構主機的 DNS 名稱指定為伺服器，並將 DN 指定為要系結至架構主機之架構容器的 DN。</span><span class="sxs-lookup"><span data-stu-id="57f59-123">Specify the DNS name of the schema master as the server and the DN as the DN of the schema container to bind to the schema master.</span></span> <span data-ttu-id="57f59-124">例如，如果伺服器是 "dc1.fabrikam.com"，而架構容器 DN 是 "cn = schema，cn = configuration，dc = fabrikam，dc = com"，ADsPath 會如下所示。</span><span class="sxs-lookup"><span data-stu-id="57f59-124">For example, if the server was "dc1.fabrikam.com" and the schema container DN was "cn=schema,cn=configuration,dc=fabrikam,dc=com", the ADsPath would be as follows.</span></span>
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

<span data-ttu-id="57f59-125">建議您尋找架構主機並系結至架構，以進行架構變更。</span><span class="sxs-lookup"><span data-stu-id="57f59-125">It is recommended that you find the schema master and bind to it to make schema changes.</span></span> <span data-ttu-id="57f59-126">不過，您可以將架構主機移至另一部伺服器。</span><span class="sxs-lookup"><span data-stu-id="57f59-126">However, you can move the schema master to another server.</span></span>

<span data-ttu-id="57f59-127">若要讓另一部伺服器成為架構主機，適當許可權的使用者可以：</span><span class="sxs-lookup"><span data-stu-id="57f59-127">To make another server the schema master, a suitably privileged user can:</span></span>

-   <span data-ttu-id="57f59-128">使用 [架構管理員] MMC 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="57f59-128">Use the Schema Manager MMC snap-in.</span></span>
    > [!Note]
    > <span data-ttu-id="57f59-129">您必須手動註冊 Active Directory 架構 MMC 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="57f59-129">The Active Directory Schema MMC snap-in must be registered manually.</span></span> <span data-ttu-id="57f59-130">若要註冊架構嵌入式管理單元，您必須從 Windows System32 目錄中的命令提示字元執行下列命令。</span><span class="sxs-lookup"><span data-stu-id="57f59-130">To register the Schema snap-in, you must run the following command from the command prompt in the Windows System32 directory.</span></span>
    >
    > <span data-ttu-id="57f59-131">**regsvr32.exe schmmgmt.dll**</span><span class="sxs-lookup"><span data-stu-id="57f59-131">**regsvr32.exe schmmgmt.dll**</span></span>

     

-   <span data-ttu-id="57f59-132">使用 NTDSUTIL 命令列公用程式。</span><span class="sxs-lookup"><span data-stu-id="57f59-132">Use the NTDSUTIL command-line utility.</span></span>
-   <span data-ttu-id="57f59-133">使用協力廠商應用程式 (會發出適當 LDAP 寫入) 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="57f59-133">Use a third-party application (an application that issues the appropriate LDAP write).</span></span>

<span data-ttu-id="57f59-134">若要以程式設計方式成為架構主機，在適當許可權使用者的內容中執行的應用程式，可以對該 DC 上的 rootDSE 發出操作屬性 **becomeSchemaMaster** 的 LDAP 寫入。</span><span class="sxs-lookup"><span data-stu-id="57f59-134">To become the schema master programmatically, an application running in the context of a suitably privileged user can issue an LDAP write of the operational attribute **becomeSchemaMaster** to the rootDSE on that DC.</span></span> <span data-ttu-id="57f59-135">這會起始將架構主機直接從目前的持有者傳送到本機 DC 的不可部分完成的傳送。</span><span class="sxs-lookup"><span data-stu-id="57f59-135">This initiates an atomic transfer of the schema master right from the current holder to the local DC.</span></span>

<span data-ttu-id="57f59-136">下列程式碼範例會尋找架構主機。</span><span class="sxs-lookup"><span data-stu-id="57f59-136">The following code example finds the schema master.</span></span> <span data-ttu-id="57f59-137">下列函式會系結至電腦上架構主機的架構容器。</span><span class="sxs-lookup"><span data-stu-id="57f59-137">The following function binds to the schema container on the computer that is the schema master.</span></span>


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



<span data-ttu-id="57f59-138">下列程式碼範例會顯示架構主機之電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="57f59-138">The following code example displays the DNS name for the computer that is the schema master.</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




