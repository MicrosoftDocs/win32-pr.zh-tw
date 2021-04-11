---
title: 顯示群組成員的範例程式碼
description: 本主題包含的程式碼範例會顯示群組的成員。
ms.assetid: 0c066bf2-65ab-47fd-bf1e-0b3192d3b4c4
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，顯示群組的成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef78c23c4a32b8a8ed36c98912f8cac24d5f375
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023240"
---
# <a name="example-code-for-displaying-members-of-a-group"></a><span data-ttu-id="9d27c-104">顯示群組成員的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="9d27c-104">Example Code for Displaying Members of a Group</span></span>

<span data-ttu-id="9d27c-105">本主題包含的程式碼範例會顯示群組的成員。</span><span class="sxs-lookup"><span data-stu-id="9d27c-105">This topic includes code examples that display members of a group.</span></span>

<span data-ttu-id="9d27c-106">下列 c + + 程式碼範例會使用 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 和 [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) 類別來顯示群組的成員。</span><span class="sxs-lookup"><span data-stu-id="9d27c-106">The following C++ code example uses the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) and [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) classes to display the members of a group.</span></span>


```C++
//////////////////////////////
/*  PrintGroupObjectMembers()    
- Prints the members of the group that the pADsGroup passes.
    Parameters
        IADsGroup * pADsGroup       - Group from which to list members.
*/
HRESULT PrintGroupObjectMembers(IADsGroup * pADsGroup)
{
    HRESULT         hr                = S_OK;     // COM Result Code
    IADsMembers *   pADsMembers       = NULL;     // Pointer to Members of the IADsGroup
    BOOL            fContinue         = TRUE;     // Looping Variable
    IEnumVARIANT *  pEnumVariant      = NULL;     // Pointer to the Enum variant
    IUnknown *      pUnknown          = NULL;     // IUnknown for getting the ENUM initially
    VARIANT         VariantArray[FETCH_NUM];      // Variant array for temp holding returned data
    ULONG           ulElementsFetched = NULL;     // Number of elements retrieved
 
    // Get an interface pointer to the IADsCollection of members.
    hr = pADsGroup->Members(&pADsMembers);
 
    if (SUCCEEDED(hr))
    {
 
        // Query the IADsCollection of members for a new ENUM Interface.
        // Be aware that the enum comes back as an IUnknown *
        hr = pADsMembers->get__NewEnum(&pUnknown);
 
        if (SUCCEEDED(hr))
        {
 
            // Call the QueryInterface method for the IUnknown * for a IEnumVARIANT interface.
            hr = pUnknown->QueryInterface(IID_IEnumVARIANT, (void **)&pEnumVariant);
 
            if (SUCCEEDED(hr))
            {
 
                // While no errors or end of data...
                while (fContinue) 
                {
                   ulElementsFetched = 0;
 
                    // Get a "batch" number of group members - number of rows that FETCH_NUM specifies
                    hr = ADsEnumerateNext(pEnumVariant, FETCH_NUM, VariantArray, &ulElementsFetched);
 
                    if (ulElementsFetched )//SUCCEEDED(hr) && hr != S_FALSE)
                    {
 
                        // Loop through the current batch, printing 
                        // the path for each member.
                        for (ULONG i = 0; i < ulElementsFetched; i++ ) 
                        {
                            IDispatch * pDispatch         = NULL; 
                            // Pointer for holding dispath of element.
                            IADs      * pIADsGroupMember  = NULL; 
                            // IADs pointer to group member.
                            BSTR        bstrPath          = NULL; 
                            // Contains the path of the object.
 
                            // Get the dispatch pointer for the variant.
                            pDispatch = VariantArray[i].pdispVal;
                            assert(HAS_BIT_STYLE(VariantArray[i].vt,VT_DISPATCH));
 
                            // Get the IADs interface for the "member" of this group.
                            hr = pDispatch->QueryInterface(IID_IADs,
                                                           (VOID **) &pIADsGroupMember) ;
 
                            if (SUCCEEDED(hr))
                            {
 
                            // Get the ADsPath property for this member.
                                hr = pIADsGroupMember->get_ADsPath(&bstrPath) ;
 
                                if (SUCCEEDED(hr))
                                {
 
                                    // Print the ADsPath of the group member.
                                    wprintf(L"\tMember Object: %ws\n", bstrPath);
                                    SysFreeString(bstrPath);
                                }
                                pIADsGroupMember->Release();
                                pIADsGroupMember   = NULL;
                            }
                         }
 
                        // Clear the variant array.
                        memset(VariantArray, 0, sizeof(VARIANT)*FETCH_NUM);
                    }
                    else
                        fContinue = FALSE;
                }
                pEnumVariant->Release();
                pEnumVariant = NULL;
            }
            pUnknown->Release();
            pUnknown = NULL;
        }
        pADsMembers ->Release();
        pADsMembers  = NULL;
    }
 
    // If all completed normally, all data
    // was printed, and an S_FALSE, indicating 
    // no more data, was received. If so,
    // return S_OK.
    if (hr == S_FALSE)
        hr = S_OK;
 
    return hr;
}
```



<span data-ttu-id="9d27c-107">下列 Visual Basic 程式碼範例會使用 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 類別來顯示群組成員。</span><span class="sxs-lookup"><span data-stu-id="9d27c-107">The following Visual Basic code example uses the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) class to display the group members.</span></span>


```VB
Sub DisplayGroupMembers(oGroup As IADsGroup)

    Dim oChild As IADs
    Dim sMembers As String

    On Error GoTo CleanUp

    MsgBox "Member Count: " & oGroup.Members.Count

    sMembers = "Names:"


    For Each oChild In oGroup.Members
        sMembers = sMembers & vbCrLf & oChild.Get("name")
    Next oChild

    MsgBox sMembers

    Exit Sub

CleanUp:
    MsgBox ("An error has occurred... " & Err.Number & vbCrLf & Err.Description)
    Set oChild = Nothing

End Sub
```



 

 