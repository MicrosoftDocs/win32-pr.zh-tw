---
title: 支援多種語言
description: 支援多種語言
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows媒體格式 SDK，支援多種語言
- Windows媒體格式 SDK，多重語言支援
- Windows媒體格式 SDK，語言支援
- Advanced Systems Format (ASF) ，支援多種語言
- ASF (Advanced Systems Format) ，支援多種語言
- Advanced Systems Format (ASF) 、多重語言支援
- ASF (Advanced Systems Format) 、多重語言支援
- Advanced Systems Format (ASF) ，語言支援
- ASF (Advanced Systems Format) ，語言支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa610d5a9b0c92fb205ecdc234a18d816190223b5bca843a542e7222695fa24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699099"
---
# <a name="to-support-multiple-languages"></a>支援多種語言

您可以在資料流程和中繼資料中支援多種語言。 Windows 媒體格式 SDK 的多重語言支援核心是 [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)介面，可維護所支援的語言清單。 語言清單會為每個支援的語言提供一個索引，此索引會在處理多種語言時用於 SDK 中的各種物件。

[**IWMLanguageList：： AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string)方法會將語言新增至清單。 您可以使用 [**IWMLanguageList：： GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) 取得語言的總數量，然後針對每個語言逐一查看呼叫 [**IWMLanguageList：： GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) 的語言，以識別已在清單中的語言。 語言索引是以零為基底。

## <a name="to-configure-mutual-exclusion-by-language"></a>依語言設定相互排除

依語言設定簡單的互斥物件非常簡單。 每個資料流程現在都與語言相關聯。 您可以使用 [**IWMStreamConfig3：： SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage)來設定與資料流程相關聯的語言。 設定所有互斥資料流程之後，只要建立相互排除的物件，就像任何其他類型一樣。 然後呼叫 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) 傳遞 CLSID \_ WMMUTEX \_ Language 作為型別。

當專有資料流程也以位元速率互斥時，語言互斥的資料流程會變得更複雜。 在此情況下，您必須執行下列步驟來使用互斥記錄：

1.  為每種語言的不同位速率資料流程建立相互排除物件。 如需以位元速率建立相互排除物件的詳細資訊，請參閱 [使用多位元率互斥](using-multiple-bit-rate-mutual-exclusion.md)。
2.  建立相互排除物件。 呼叫 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) 並傳遞 CLSID \_ WMMUTEX \_ 語言，以指定獨佔性 by language。
3.  藉由呼叫 [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)的 **QueryInterface** 方法，取得在步驟2中建立之相互排除物件的 [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)介面指標。
4.  針對每個語言呼叫 [**IWMMutualExclusion2：： AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) 方法一次，以建立將會互斥的資料流程記錄。
5.  針對在步驟4中建立的每一筆記錄，使用 [**IWMMutualExclusion2：： AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord)的呼叫新增適當語言的資料流程。

## <a name="to-read-files-with-multiple-languages"></a>讀取具有多種語言的檔案

Reader 物件提供方法，以識別檔案中資料流程的可用語言。 您可以藉由呼叫 [**IWMReaderAdvanced4：： GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount)，來取得輸出的支援語言數目。 然後，您可以呼叫 [**IWMReaderAdvanced4：： GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage)來取得每個語言的詳細資料。

您可以藉由呼叫 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)，將該語言的索引傳遞給讀取器，以指定要播放的語言。 這會選取指定的語言，同時為檔案中的任何其他互斥物件維持自動資料流程選取。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Advanced 主題**](advanced-topics.md)
</dt> <dt>

[**IWMLanguageList 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**IWMMutualExclusion 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMMutualExclusion2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**IWMReaderAdvanced2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMReaderAdvanced4 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**IWMStreamConfig3 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




