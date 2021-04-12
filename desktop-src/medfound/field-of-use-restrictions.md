---
description: 使用限制領域
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: 使用限制領域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16f57de7642fa789a08c886a32bf906faffb72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317964"
---
# <a name="field-of-use-restrictions"></a>使用限制領域

> [!Note]  
> 本主題適用于 Windows 7 或更新版本。

 

*使用* 規定限制是一種規定，可限制特定技術授權的使用方式。

媒體基礎提供一種機制，可在媒體基礎轉換 (MFTs) （特別是編解碼器）上強制執行限制的限制。 這項機制需要使用 MFT 來封鎖應用程式的使用，直到應用程式執行與 MFT 之間的交握為止。 媒體基礎不會定義交握，通常會牽涉到某種類型的密碼編譯交換。

### <a name="registration-and-enumeration"></a>註冊和列舉

如果某個 MFT 有使用中的限制，請在您註冊 MFT 時設定 **mft \_ 列舉 \_ 旗標 \_ FIELDOFUSE** 旗標。 此旗標適用于下列的 MFT 註冊 Api：

-   [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**IMFLocalMFTRegistration::RegisterMFTs**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

根據預設，使用此旗標注冊的 MFTs 會從列舉結果中排除。 若要以使用中的限制列舉 MFTs，請呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 並在 Flags 參數中指定 **MFT \_ 列舉 \_ 旗標 \_ FIELDOFUSE** 旗 *標* 。 下圖說明此程序。

![顯示 mft 和應用程式將資料傳送至登錄的圖表](images/mft-fou01.gif)

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)函數一律會排除具有使用規定限制的任何 MFTs。

### <a name="unlocking-the-mft"></a>解除鎖定 MFT

若要搭配使用具有欄位限制的 MFT，請執行下列步驟：

1.  應用程式會執行 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 介面。
2.  [**IMFFieldOfUseMFTUnlock：： Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock)方法會接受對 MFT 之 **IUnknown** 介面的指標。
3.  在 [**解除鎖定**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) 方法中，應用程式會使用由 MFT 定義的任何機制來執行所需的交握。 媒體基礎 API 不會定義此步驟。
4.  如果 [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) 方法成功，則是由 MFT 解除鎖定。

應用程式會藉由設定 [MFT \_ FIELDOFUSE \_ UNLOCK \_ Attribute](mft-fieldofuse-unlock-attribute.md)屬性來指定 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)指標。 有幾種不同的方式可以設定此屬性，端視您的應用程式建立解碼器或編碼管線的方式而定：



| API                   | 如何解除鎖定使用中的欄位                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 來源讀取程式         | 如果您的應用程式使用 [來源讀取器](source-reader.md) 來解碼媒體檔案，請在設定參數中設定 [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md) 屬性。 請參閱 [來源讀取器屬性](source-reader-attributes.md)。                                                                                                                                                                                                                                                                         |
| 接收寫入器           | 如果您的應用程式使用接收寫入器來編碼媒體檔案，請在設定參數中設定 [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md) 屬性。 請參閱 [接收寫入器屬性](sink-writer-attributes.md)。                                                                                                                                                                                                                                                                                                    |
| 快速轉碼        | 如果您的應用程式使用快速轉碼功能來建立編碼拓撲，請在呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)時設定 [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)。 如需快速轉碼功能的詳細資訊，請參閱 [轉碼 API](transcode-api.md)。                                                                                                                                                                      |
| 拓撲              | 如果您直接建立拓撲，請將 [ [MFT \_ FIELDOFUSE \_ 解除鎖定] \_ 屬性](mft-fieldofuse-unlock-attribute.md) 設定為拓撲上的屬性。 請參閱 [拓撲屬性](topology-attributes.md)。                                                                                                                                                                                                                                                                                                                                                  |
| MFT 啟用物件 | 如果您的應用程式直接列舉將使用的解碼器或編碼器，請在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定 [MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性](mft-fieldofuse-unlock-attribute.md)。 <br/> 先設定屬性再呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ，以建立 MFT。 啟始物件會在建立 MFT 時呼叫 [**IMFFieldOfUseMFTUnlock：： Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) 。<br/> |



 

下圖顯示 MFT 啟用物件和 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) 介面之間的關聯性。

![此圖顯示應用程式、啟用物件和包含箭號給 fou ... 物件的 mft，此物件的箭號會傳回給 mft](images/mft-fou02.gif)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 




