---
description: 表示與憑證相關聯的私密金鑰。
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: PrivateKey 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e74720cac1287c08209ce08cabe7b364d385412d94213a83bd114dc46605b7ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977634"
---
# <a name="privatekey-object"></a>PrivateKey 物件

\[**PrivateKey** 物件可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]

**PrivateKey** 物件代表與憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md)。

## <a name="when-to-use"></a>使用時機

**PrivateKey** 物件是用來執行下列工作：

-   取得私密金鑰的相關資訊。
-   開啟私密金鑰容器。
-   刪除私密金鑰。

## <a name="members"></a>成員

**PrivateKey** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**PrivateKey** 物件有這些方法。



| 方法                                                  | 描述                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**刪除**](privatekey-delete.md)                     | 刪除 **PrivateKey** 物件所參考的私用金鑰容器。<br/>                                                                                |
| [**IsAccessible**](privatekey-isaccessible.md)         | 抓取布林值，指出使用者是否可以存取私密金鑰。 若為 true，則使用者可以存取私密金鑰。<br/>                 |
| [**IsExportable**](privatekey-isexportable.md)         | 抓取布林值，指出是否可以匯出私密金鑰。 若為 true，則可以匯出私密金鑰。<br/>                               |
| [**IsHardwareDevice**](privatekey-ishardwaredevice.md) | 抓取布林值，指出私密金鑰是否儲存在硬體裝置上。 若為 true，則會將私密金鑰儲存在硬體裝置上。<br/> |
| [**IsMachineKeyset**](privatekey-ismachinekeyset.md)   | 抓取布林值，指出私密金鑰是否為電腦金鑰。 若為 true，則私密金鑰為電腦金鑰。<br/>                             |
| [**IsProtected**](privatekey-isprotected.md)           | 抓取布林值，指出私密金鑰是否受到保護。 若為 true，則會保護私密金鑰。<br/>                                     |
| [**IsRemovable**](privatekey-isremovable.md)           | 抓取布林值，指出私密金鑰是否在可移動裝置上。 若為 true，則私密金鑰位於卸載式裝置上。<br/>             |
| [**打開**](privatekey-open.md)                         | 存取現有的金鑰容器。<br/>                                                                                                                       |



 

### <a name="properties"></a>屬性

**PrivateKey** 物件具有這些屬性。



| 屬性                                                                 | 存取類型          | 描述                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [**容器**](privatekey-containername.md)<br/>             | 唯讀<br/> | 抓取包含私密金鑰容器名稱的字串。 這是預設屬性。<br/> |
| [**KeySpec**](privatekey-keyspec.md)<br/>                         | 唯讀<br/> | 抓取金鑰規格。<br/>                                                               |
| [**ProviderName**](privatekey-providername.md)<br/>               | 唯讀<br/> | 抓取包含 CSP 名稱的字串。<br/>                                          |
| [**ProviderType**](privatekey-providertype.md)<br/>               | 唯讀<br/> | 抓取指定提供者類型的列舉值。<br/>                            |
| [**UniqueContainerName**](privatekey-uniquecontainername.md)<br/> | 唯讀<br/> | 抓取包含唯一私用金鑰容器名稱的字串。<br/>                        |



 

## <a name="remarks"></a>備註

您可以建立 **PrivateKey** 物件，而且可以安全地進行腳本處理。 **PrivateKey** 物件的 PROGID 是 CAPICOM。PrivateKey。1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
