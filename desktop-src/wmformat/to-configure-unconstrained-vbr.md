---
title: 設定未受限制的 VBR
description: 設定未受限制的 VBR
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- 串流，設定 VBR 資料流程
- '資料流程、變數位元速率 (VBR) '
- 變數位速率 (VBR) ，資料流程
- VBR (變數位速率) ，資料流程
- 資料流程，設定未受限制的 VBR
- 變數位元速率 (VBR) ，設定不受限制
- VBR (變數位速率) ，設定不受限制
- 設定檔，設定未受限制的 VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092581"
---
# <a name="to-configure-unconstrained-vbr"></a>設定未受限制的 VBR

您可以在資料流程上使用不受限制的變數位元速率 (VBR) 編碼方式，以指定將在編碼內容中維護的平均位元速率。 未受限制的 VBR 與一般 CBR 不同之處在于，在整個資料流程中，位元速率的變異數可能更大。

資料流程的位元速率（以 [**IWMStreamConfig：： SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)設定）是用來做為所需的平均位元速率。 當資料流程的編碼完成時，您可以使用 [**IWMPropertyVault：： GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) 抓取兩個額外的屬性： **g \_ wszVBRPeak** 和 **g \_ wszBufferAverage**。 這些屬性會分別描述編碼內容的尖峰位元速率，以及內容的平均緩衝區視窗。

未受限制的 VBR 必須搭配雙通編碼使用。 設定檔中未設定雙通編碼。 您必須將寫入器設定為在寫入資料流程之前執行前置處理階段。 如需使用雙通編碼的詳細資訊，請參閱 [使用 Two-Pass 編碼](using-two-pass-encoding.md)。

若要將設定檔中的串流設定為使用未受限制的 VBR 進行編碼，請執行下列步驟：

1.  藉由呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數來建立配置檔案管理員物件。
2.  開啟您要新增 VBR 支援的現有設定檔。 如需開啟設定檔的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。
3.  藉由呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) 或 [**IWMProfile：： GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)，取得您想要使用之資料流程的資料流程設定物件。
4.  藉由呼叫 **IWMStreamConfig：： QueryInterface**，取得資料流程設定物件之 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)介面的指標。
5.  針對 **g \_ wszVBREnabled** 屬性呼叫 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) ，以啟用資料流程的 VBR 編碼。
6.  使用 **IWMPropertyVault：： SetProperty** 將 **g \_ wszVBRBitrateMax** 和 **g \_ wszVBRBufferWindowMax** 兩者都設定為零。
7.  藉由呼叫 [**IWMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)，儲存對資料流程所做的變更。
8.  儲存設定檔，或將其傳遞至寫入器物件。
9.  設定寫入器以執行前置處理階段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定 VBR 資料流程**](configuring-vbr-streams.md)
</dt> </dl>

 

 




