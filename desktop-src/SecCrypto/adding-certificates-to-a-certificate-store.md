---
description: 如果存放區是以讀取/寫入權限開啟，則可以在憑證存放區中新增或移除憑證。
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: 將憑證新增至憑證存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513484"
---
# <a name="adding-certificates-to-a-certificate-store"></a>將憑證新增至憑證存放區

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

如果存放區是以讀取/寫入權限開啟，則可以在 [*憑證存放區*](../secgloss/c-gly.md)中新增或移除 [*憑證*](../secgloss/c-gly.md)。 未將讀取/寫入權限授與 Active Directory 存放區。 雖然可以在記憶體存放區中新增或移除憑證，但記憶體存放區中的變更不會在會話之間保存。

您可以使用 **Add** 方法，將憑證新增至以讀取/寫入權限開啟的憑證存放區中。 您可以使用 **Remove** 方法，從以讀取/寫入權限開啟的憑證存放區中移除憑證。 新的存放區可以在 CAPICOM \_ 目前的 \_ 使用者 \_ 存放區和 capicom \_ 本機 \_ 電腦 \_ 存放區位置中建立及儲存。 您可以使用讀取/寫入權限開啟其中一個位置的新建立的存放區。

下列範例會開啟兩個憑證存放區。 以 F 開頭的主體憑證會從 Active Directory 存放區中取出。 \_ \_ 接著，會將 capicom 目前使用者 \_ 存放區、capicom \_ ca \_ 存放區存放區開啟為讀取/寫入存放區，並將 Active Directory 存放區中憑證集合的第一個憑證新增到 CAPICOM \_ CA 存放區中的憑證 \_ 。

基於示範目的，此範例會顯示在 CAPICOM 記憶體存放區中開啟存放區 \_ \_ 、將目前的 \_ \_ 使用者 \_ 存放區，以及 capicom \_ 本機 \_ 電腦 \_ 存放區位置。 此範例顯示如何從開啟的存放區匯出所有憑證、將匯出的憑證寫入檔案、將其讀取，以及將它們匯入至不同的存放區。 新匯入的憑證會列舉並顯示。

在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。 如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。 如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。

下列範例示範如何在 **存放區** 物件的宣告中使用早期繫結來開啟憑證存放區，以及建立這些物件的實例。


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
