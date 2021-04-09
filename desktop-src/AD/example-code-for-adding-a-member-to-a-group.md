---
title: 將成員新增至群組的範例程式碼
description: 本主題包含將成員新增至群組的程式碼範例。
ms.assetid: 306fcadb-a492-41e5-bfb3-8beaaec24fb5
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，將成員新增至群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a64a41fac871c6793ee4d0db1f4be79c9fbd0d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933720"
---
# <a name="example-code-for-adding-a-member-to-a-group"></a><span data-ttu-id="9853d-104">將成員新增至群組的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="9853d-104">Example Code for Adding a Member to a Group</span></span>

<span data-ttu-id="9853d-105">本主題包含將成員新增至群組的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="9853d-105">This topic contains code examples that add a member to a group.</span></span> <span data-ttu-id="9853d-106">Visual Basic Scripting Edition (VBScript) 和 c + + 範例加入成員，方法是將代表該成員的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 物件新增至代表該群組的 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 物件。</span><span class="sxs-lookup"><span data-stu-id="9853d-106">The Visual Basic Scripting Edition (VBScript) and C++ examples add a member by adding the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) object that represents the member to the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) object that represents the group.</span></span> <span data-ttu-id="9853d-107">Visual Basic .NET 和 c # 範例會修改代表群組之 [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) 物件的成員屬性。</span><span class="sxs-lookup"><span data-stu-id="9853d-107">The Visual Basic .NET and C# examples modify the member property of the [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span>


<span data-ttu-id="9853d-108">下列 c # 程式碼範例會將現有的成員新增至群組。</span><span class="sxs-lookup"><span data-stu-id="9853d-108">The following C# code examples add an existing member to a group.</span></span> <span data-ttu-id="9853d-109">函數會採用群組容器的 ADsPath，以及要加入至群組之成員的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="9853d-109">The function takes the ADsPath of the group container and the distinguished name of the member to be added to the group.</span></span> <span data-ttu-id="9853d-110">ADsPath 用來建立代表群組的 [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) 物件。</span><span class="sxs-lookup"><span data-stu-id="9853d-110">The ADsPath is used to create a [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span> <span data-ttu-id="9853d-111">[PropertyValueCollection](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_)新增方法會將辨別名稱傳遞至函式的成員加入群組中。</span><span class="sxs-lookup"><span data-stu-id="9853d-111">The [PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) method adds to the group the member whose distinguished name was passed to the function.</span></span> <span data-ttu-id="9853d-112">然後，函數會使用 [CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) 方法，將新的成員資訊寫入資料庫。</span><span class="sxs-lookup"><span data-stu-id="9853d-112">The function then uses the [DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) method to write the new member information to the database.</span></span>

<span data-ttu-id="9853d-113">使用下列參數呼叫函數：</span><span class="sxs-lookup"><span data-stu-id="9853d-113">Call the function with the following parameters:</span></span>

-   <span data-ttu-id="9853d-114">*bindString*：群組容器的有效 ADsPath，例如 "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"</span><span class="sxs-lookup"><span data-stu-id="9853d-114">*bindString*: a valid ADsPath for a group container, such as "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"</span></span>
-   <span data-ttu-id="9853d-115">*>newmember*：要新增至群組之成員的辨別名稱，例如 "CN = JEFFSMITH，OU = TESTOU，DC = FABRIKAM，DC = com"</span><span class="sxs-lookup"><span data-stu-id="9853d-115">*newMember*: the distinguished name of the member to be added to the group, such as "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"</span></span>


```CSharp
private void AddMemberToGroup(

                                string bindString,

                                string newMember

                                )

{

    try
    {

        DirectoryEntry ent = new DirectoryEntry( bindString );

        ent.Properties["member"].Add(newMember);

        ent.CommitChanges();

    }

    catch (Exception e)
    {

        Console.WriteLine( "An error occurred.");

        Console.WriteLine( "{0}", e.Message);

        return;

    }

}
```




<span data-ttu-id="9853d-116">下列 Visual Basic .NET 程式碼範例會將現有的成員新增至群組。</span><span class="sxs-lookup"><span data-stu-id="9853d-116">The following Visual Basic .NET code examples add an existing member to a group.</span></span> <span data-ttu-id="9853d-117">函數會採用群組容器的 ADsPath，以及要加入至群組之成員的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="9853d-117">The function takes the ADsPath of the group container and the distinguished name of the member to be added to the group.</span></span> <span data-ttu-id="9853d-118">ADsPath 用來建立代表群組的 [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) 物件。</span><span class="sxs-lookup"><span data-stu-id="9853d-118">The ADsPath is used to create a [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span> <span data-ttu-id="9853d-119">[PropertyValueCollection](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_)新增方法會將辨別名稱傳遞至函式的成員加入群組中。</span><span class="sxs-lookup"><span data-stu-id="9853d-119">The [PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) method adds to the group the member whose distinguished name was passed to the function.</span></span> <span data-ttu-id="9853d-120">然後，函數會使用 [CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) 方法，將新的成員資訊寫入資料庫。</span><span class="sxs-lookup"><span data-stu-id="9853d-120">The function then uses the [DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) method to write the new member information to the database.</span></span>

<span data-ttu-id="9853d-121">使用下列參數呼叫函數：</span><span class="sxs-lookup"><span data-stu-id="9853d-121">Call the function with the following parameters:</span></span>

-   <span data-ttu-id="9853d-122">*bindString*：群組容器的有效 ADsPath，例如 "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"</span><span class="sxs-lookup"><span data-stu-id="9853d-122">*bindString*: a valid ADsPath for a group container, such as "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"</span></span>
-   <span data-ttu-id="9853d-123">*>newmember*：要新增至群組之成員的辨別名稱，例如 "CN = JEFFSMITH，OU = TESTOU，DC = FABRIKAM，DC = com"</span><span class="sxs-lookup"><span data-stu-id="9853d-123">*newMember*: the distinguished name of the member to be added to the group, such as "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"</span></span>


```VB
Private Sub AddMemberToGroup(ByVal bindString As String, 
                                      ByVal newMember As String)

    Try

        Dim ent As New DirectoryEntry(bindString)

        ent.Properties("member").Add(newMember)

        ent.CommitChanges()

    Catch e As Exception

        Console.WriteLine("An error occurred.")

        Console.WriteLine("{0}", e.Message)

        Return

    End Try

End Sub
```




<span data-ttu-id="9853d-124">下列 VBScript 範例會將現有的成員新增至群組。</span><span class="sxs-lookup"><span data-stu-id="9853d-124">The following VBScript example adds an existing member to a group.</span></span> <span data-ttu-id="9853d-125">腳本會將 Jeff Smith 的使用者新增至 TestGroup 群組。</span><span class="sxs-lookup"><span data-stu-id="9853d-125">The script adds the user, Jeff Smith, to the TestGroup group.</span></span>


```VB
Option Explicit

On Error Resume Next

Dim scriptResult        ' Script success or failure

Dim groupPath           ' ADsPath to the group container

Dim group               ' Group object

Dim memberPath          ' ADsPath to the member

Dim member              ' Member object

Dim groupMemberList     ' Used to display group members

Dim errorText           ' Error handing text

scriptResult = False

groupPath = "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"

memberPath = "LDAP://CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"

WScript.Echo("Retrieving group object")

Set group = GetObject(groupPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not create group object.")

End If

Call ShowMembers(groupPath)     'Optional function call

WScript.Echo("Retrieving new member object")

Set member = GetObject(memberPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not get new member object.")

End If

WScript.Echo("Adding member to group.")

group.Add(member.ADsPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not add member to group.")

End If

Call ShowMembers(groupPath)     ' Optional function call

scriptResult = True

Call FinalResult(scriptResult)

'****************************************************************
' This function displays the members of a group. The function
' takes the ADsPath of the group.
'****************************************************************

Sub ShowMembers(groupPath)

    Dim groupMember

    Dim groupMemberList

    Dim groupObject

    Set groupObject = GetObject(groupPath)

    Set groupMemberList = groupObject.Members

    Select Case groupMemberList.Count

        Case 1 

            WScript.Echo vbcrlf & "The group has one member."

        Case 0

            WScript.Echo vbcrlf & "The group has no members."

        Case Else

            WScript.Echo vbcrlf & "The group has " & groupMemberList.Count & " members."

    End Select

    If groupMemberList.Count > 0 then

        WScript.Echo vbcrlf & "Here is a member list."

        For Each groupMember in groupMemberList

            WScript.Echo groupMember.Name

        Next

        WScript.Echo vbcrlf

    End If

    Set groupObject = Nothing

    Set groupMemberList = Nothing

End Sub

'****************************************************************
' This function shows if the script succeeded or failed. The 
' function processed the scriptResult variable.
'****************************************************************

Sub FinalResult(scriptResult)

    WScript.Echo vbcrlf

    If scriptResult = False then

        WScript.Echo "Script failed."

    Else

        WScript.Echo("Script successfully completed.")

    End If

    WScript.Quit

End Sub

'****************************************************************
' This function handles errors that occur in the script.
'****************************************************************

Sub ErrorHandler( errorText )

    WScript.Echo(vbcrlf & errorText)

    WScript.Echo("Error number: " & Err.number)

    WScript.Echo("Error Description: " & Err.Description)

    Err.Clear 

    Call FinalResult(scriptResult)

End Sub

```




<span data-ttu-id="9853d-126">下列 c + + 程式碼範例會將現有的成員新增至群組。</span><span class="sxs-lookup"><span data-stu-id="9853d-126">The following C++ code example adds an existing member to a group.</span></span>


```C++
/////////////////////////////////////////////////////////////
/*  AddMemberToGroup() - Adds the passed directory object as a member 
                         of passed group
 
    Parameters
 
        IADsGroup * pGroup   - Group to hold the new IDirectoryObject.
        IADs* pIADsNewMember - Object which will become a member 
                               of the group. Object can be a user, 
                               contact, or group.
*/
HRESULT AddMemberToGroup(IADsGroup * pGroup, IADs* pIADsNewMember)
{
    HRESULT hr = E_INVALIDARG;
    if ((!pGroup)||(!pIADsNewMember))
        return hr;
 
    // Use the IADs::get_ADsPath() member to get the ADsPath.
    // When the ADsPath string is returned, to add the new
    // member to the group, call the IADsGroup::Add() member,
    // passing in the ADsPath string.
    // Query the new member for its AdsPath.
    // This is a fully qualified LDAP path to the object to add.
    BSTR bsNewMemberPath;
    hr = pIADsNewMember->get_ADsPath(&bsNewMemberPath); 
    if (SUCCEEDED(hr))
    {
 
        // Use the IADsGroup interface to add the new member.
        // Pass the LDAP path to the 
        // new member to the IADsGroup::Add() member
        hr = pGroup->Add(bsNewMemberPath);
 
        // Free the string returned from IADs::get_ADsPath()
        SysFreeString(bsNewMemberPath);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9853d-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9853d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9853d-128">將成員新增至網域中的群組</span><span class="sxs-lookup"><span data-stu-id="9853d-128">Adding Members to Groups in a Domain</span></span>](adding-members-to-groups-in-a-domain.md)
</dt> <dt>

[<span data-ttu-id="9853d-129">DirectoryEntry</span><span class="sxs-lookup"><span data-stu-id="9853d-129">DirectoryEntry</span></span>](/dotnet/api/system.directoryservices.directoryentry)
</dt> <dt>

[<span data-ttu-id="9853d-130">DirectoryEntry. CommitChanges</span><span class="sxs-lookup"><span data-stu-id="9853d-130">DirectoryEntry.CommitChanges</span></span>](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges)
</dt> <dt>

[<span data-ttu-id="9853d-131">**IADs**</span><span class="sxs-lookup"><span data-stu-id="9853d-131">**IADs**</span></span>](/windows/desktop/api/iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="9853d-132">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="9853d-132">**IADsGroup**</span></span>](/windows/desktop/api/iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="9853d-133">PropertyValueCollection 新增</span><span class="sxs-lookup"><span data-stu-id="9853d-133">PropertyValueCollection.Add</span></span>](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_)
</dt> </dl>

 

 