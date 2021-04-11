---
description: 下列範例示範如何使用 Visual Basic for Applications (VBA) 副程式來填入 MsiDigitalCertificate 資料表和 MsiDigitalSignature 資料表。
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: 使用自動化撰寫經過完整驗證的已簽署安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99267feffac71401f36635c08fa7f9f6598a0c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944014"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>使用自動化撰寫經過完整驗證的已簽署安裝

下列範例示範如何使用 Visual Basic for Applications (VBA) 副程式來填入 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md) 和 [MsiDigitalSignature 資料表](msidigitalsignature-table.md) 。 如需保護 Windows Installer 套件安全的詳細資訊，請參閱 [撰寫安全安裝的指導方針](guidelines-for-authoring-secure-installations.md)。

[**FileSignatureInfo 方法**](installer-filesignatureinfo.md)會傳回位元組的 SAFEARRAY。 如需詳細資訊，請參閱 [**SAFEARRAY 資料類型**](/windows/win32/api/oaidl/ns-oaidl-safearray)。 此陣列中的資料必須轉換成 Unicode，因為 Visual Basic 沒有方法可直接將位元組寫入檔案。 然後， [**SetStream 方法**](record-setstream.md) 可以使用已轉換資料的檔案，將資料流程資料寫入至 [**記錄物件**](record-object.md)的指定記錄欄位。 請注意，將位元組資料轉換成 Unicode 可能會變更資料，而轉換的資料必須符合原始資料以進行正確的簽章驗證。 封裝作者必須確保原始和已轉換的資料相符。


```VB
Sub PopulateDigitalSignature()

    Dim Installer As Object
    Dim Database As Object
    Dim x() As Byte
    
    Const szSignedCabinet = "c:\test.cab"
    Const szCertFile = "c:\temp\test.cer"
    Const szDatabase = "c:\test.msi"
        
    Set Installer = CreateObject("WindowsInstaller.Installer")
    
    x = Installer.FileSignatureInfo(szSignedCabinet, 0, msiSignatureInfoCertificate)
    
    Dim fs, ts
    Dim s As String
    Set fs = CreateObject("Scripting.FileSystemObject")
    Set ts = fs.CreateTextFile(szCertFile, True)        'Create a file
    
    s = StrConv(x, vbUnicode)
    ts.Write s
    ts.Close
        
    Set Database = Installer.OpenDatabase(szDatabase, msiOpenDatabaseModeTransact)
    Set ViewCert = Database.OpenView("SELECT * FROM `MsiDigitalCertificate`")
    ViewCert.Execute 0
    Set ViewSig = Database.OpenView("SELECT * FROM `MsiDigitalSignature`")
    ViewSig.Execute 0
    
    Set RecordCert = Installer.CreateRecord(2)
    RecordCert.StringData(1) = "Test"
    RecordCert.SetStream 2, szCertFile
    ViewCert.Modify msiViewModifyInsert, RecordCert
    
    Set RecordSig = Installer.CreateRecord(4)
    RecordSig.StringData(1) = "Media"
    RecordSig.StringData(2) = "1"
    RecordSig.StringData(3) = "Test"
    ViewSig.Modify msiViewModifyInsert, RecordSig
    
    Database.Commit
      fs.DeleteFile(szCertFile)
End Sub
```



 

 
