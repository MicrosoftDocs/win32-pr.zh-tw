---
description: 提供使用 Authenticode 數位簽章來簽署可執行檔的功能。
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: SignedCode 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984861"
---
# <a name="signedcode-object"></a>SignedCode 物件

\[**SignedCode** 物件可用於 [需求] 區段中指定的作業系統。 相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**SignedCode** 物件提供使用 Authenticode 數位簽章來簽署可執行檔的功能。

## <a name="when-to-use"></a>使用時機

**SignedCode** 物件是用來執行下列工作：

-   簽署可執行檔。
-   時間戳記可執行檔。
-   判斷可執行檔的簽章是否有效。
-   設定或取得可執行檔的路徑。
-   取得可執行檔的簽署者和時間戳記程式。
-   取得可執行檔的憑證集合。
-   取得可執行檔描述的描述或 URL。

## <a name="members"></a>成員

**SignedCode** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SignedCode** 物件有這些方法。



| 方法                                    | 描述                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**標誌**](signedcode-sign.md)           | 建立 Authenticode 數位簽章，並簽署 [**SignedCode**](signedcode-filename.md) 中指定的可執行檔。<br/>    |
| [**時間 戳**](signedcode-timestamp.md) | 在 [**SignedCode**](signedcode-filename.md) 中指定的已簽署可執行檔上建立 Authenticode 時間戳記簽章。<br/> |
| [**驗證**](signedcode-verify.md)       | 驗證 [**SignedCode**](signedcode-filename.md) 中指定之已簽署可執行檔的 Authenticode 簽章。<br/>          |



 

### <a name="properties"></a>屬性

**SignedCode** 物件具有這些屬性。



| 屬性                                                       | 存取類型           | Description                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**憑證**](signedcode-certificates.md)<br/>     | 唯讀<br/>  | [**憑證**](certificates.md)集合，其中包含已簽署之可執行檔中的所有憑證。<br/>             |
| [**描述**](signedcode-description.md)<br/>       | 讀取/寫入<br/> | 字串，其中包含已簽署之可執行檔的描述。<br/>                                                             |
| [**DescriptionURL**](signedcode-descriptionurl.md)<br/> | 讀取/寫入<br/> | 字串，其中包含已簽署可執行檔之描述的 HTTP 位址。<br/>                                         |
| [**檔案名**](signedcode-filename.md)<br/>             | 讀取/寫入<br/> | 字串，包含包含可執行檔之內容檔的路徑。<br/> 這是預設屬性。<br/> |
| [**簽署者**](signedcode-signer.md)<br/>                 | 唯讀<br/>  | [**簽署者**](signer.md)物件，可存取可執行檔的簽署者。<br/>                                    |
| [**Timestamper**](signedcode-timestamper.md)<br/>       | 唯讀<br/>  | [**簽署者**](signer.md)物件，可存取可執行檔的時間戳記程式。<br/>                              |



 

## <a name="remarks"></a>備註

您可以建立 **SignedCode** 物件，而且對腳本而言並不安全。 **SignedCode** 物件的 PROGID 是 CAPICOM。SignedCode。1。

可執行檔的類型應為可使用 Authenticode 技術簽署的型別，例如副檔名為 .cab、.cat、.exe、.dll、.vbs 或 .ocx 的檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
