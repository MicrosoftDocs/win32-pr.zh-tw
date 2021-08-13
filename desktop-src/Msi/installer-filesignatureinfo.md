---
description: 安裝程式物件的 FileSignatureInfo 方法會取得檔案的路徑，並傳回代表雜湊或編碼憑證的位元組的 SAFEARRAY。
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: FileSignatureInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 670b5ba6deb4a53429180e832c2a49e4968c53efbe7c54cdf50e62e20bf5503b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630779"
---
# <a name="installerfilesignatureinfo-method"></a>FileSignatureInfo 方法

[**安裝程式**](installer-object.md)物件的 **FileSignatureInfo** 方法會取得檔案的路徑，並傳回代表雜湊或編碼憑證的位元組的 SAFEARRAY。 然後可以使用這些值來填入 [MsiDigitalSignature](msidigitalsignature-table.md)、 [MsiPatchCertificate](msipatchcertificate-table.md)和 [MsiDigitalCertificate](msidigitalcertificate-table.md) 資料表。

如需詳細資訊，請參閱 [**SAFEARRAY 資料類型**](/windows/win32/api/oaidl/ns-oaidl-safearray)。

## <a name="syntax"></a>語法


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*FilePath* 
</dt> <dd>

經過數位簽署之檔案的完整路徑。

填入 [MsiDigitalSignature](msidigitalsignature-table.md) 和 [MsiDigitalCertificate](msidigitalcertificate-table.md) 資料表時， *FilePath* 會指向數位簽署的封包。 填入 [MsiPatchCertificate](msipatchcertificate-table.md) 和 MsiDigitalCertificate 資料表時， *FilePath* 會指向經過數位簽署的修補程式。

</dd> <dt>

*選項* 
</dt> <dd>

特殊的錯誤案例旗標。



| 旗標                                                                                                                                                                                                                                                                                                                                    | 意義                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | 當 *選項* 設定為 msiSignatureOptionInvalidHashFatal 時， **FileSignatureInfo** 一律會傳回無效雜湊的嚴重錯誤。 <br/> 如果 *選項* 未設定為 msiSignatureOptionInvalidHashFatal，而且 *Format* 設定為 msiSignatureInfoCertificate，則 **FileSignatureInfo** 不會針對不正確雜湊傳回錯誤。<br/> |



 

</dd> <dt>

*格式* 
</dt> <dd>

要求的簽章資訊。



| 旗標                                                                                                                                                                                                                                                                                                        | 意義                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | 傳回代表編碼憑證的位元組的 SAFEARRAY。<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | 傳回表示雜湊的位元組的 SAFEARRAY。<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，方法會傳回包含雜湊或編碼憑證的位元組的 [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) 。

## <a name="remarks"></a>備註

若要使用 automation 來撰寫經過完整驗證的已簽署安裝，請使用 **FileSignatureInfo** 方法來填入 [MsiDigitalCertificate](msidigitalcertificate-table.md)、 [MsiPatchCertificate](msipatchcertificate-table.md)和 [MsiDigitalSignature](msidigitalsignature-table.md) 資料表。 如需詳細資訊，請參閱 [使用自動化撰寫經過完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation-using-automation.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用自動化撰寫經過完整驗證的已簽署安裝](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
