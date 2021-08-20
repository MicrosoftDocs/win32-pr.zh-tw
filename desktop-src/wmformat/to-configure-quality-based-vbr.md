---
title: 設定 Quality-Based VBR
description: 設定 Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- 串流，設定 VBR 資料流程
- '資料流程、變數位元速率 (VBR) '
- 變數位速率 (VBR) ，資料流程
- VBR (變數位速率) ，資料流程
- 串流，設定以品質為基礎的 VBR
- 變數位元速率 (VBR) ，設定品質型
- VBR (變數位元速率) ，設定品質型
- 設定檔，設定以品質為基礎的 VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b1181d722909478b29e1ffbe5f5b53cb919d80e3922e055eecdf34c334a382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845633"
---
# <a name="to-configure-quality-based-vbr"></a>設定 Quality-Based VBR

您可以在資料流程上使用以品質為基礎的變數位元速率 (VBR) 編碼方式，以指定將針對整個資料流程維護的品質等級，不論產生的位元速率需求為何。

針對品質型的 VBR 影片串流，您必須指定從1到100的品質等級，100表示最高品質。 目前只有30個離散品質設定。 下列品質層級等於離散品質設定：1、4、8、11、15、18、22、25、29、33、36、40、43、47、50、54、58、61、65、68、72、75、79、83、86、90、93、97。 上述清單中兩個連續值之間的數位，會等於與較低數位相同的品質設定。 例如，系統會列出1和4，因此2和3兩者都會產生與1相同的品質設定。

針對音訊串流，您可以列舉可用的模式並取出串流設定物件。 如需詳細資訊，請參閱 [列舉編解碼器格式](to-enumerate-codec-formats.md)。

使用以品質為基礎的 VBR 影片時，您必須將 [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)結構的 **dwBitrate** 成員設為正值。 寫入器不會使用這個值，但傳遞零或負數可能會在寫入時發生錯誤。

若要在設定檔中設定串流以以品質為基礎的 VBR 進行編碼，請執行下列步驟。

1.  藉由呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數來建立配置檔案管理員物件。
2.  開啟您要新增 VBR 支援的現有設定檔。 如需開啟設定檔的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。
3.  藉由呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) 或 [**IWMProfile：： GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)，取得您想要使用之資料流程的資料流程設定物件。
4.  藉由呼叫 **IWMStreamConfig：： QueryInterface**，取得資料流程設定物件之 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)介面的指標。
5.  針對 **g \_ wszVBREnabled** 屬性呼叫 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) ，為數據流啟用 VBR。
6.  針對 **g \_ wszVBRQuality** 屬性呼叫 **IWMPropertyVault：： SETPROPERTY** ，以設定 VBR 資料流程的品質等級。
7.  使用 **IWMPropertyVault：： SetProperty** 將 **g \_ wszVBRBitrateMax** 和 **g \_ wszVBRBufferWindowMax** 兩者都設定為零。
8.  藉由呼叫 [**IWMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)，儲存對資料流程所做的變更。
9.  儲存設定檔，或將其傳遞至寫入器物件，然後開始撰寫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定 VBR 資料流程**](configuring-vbr-streams.md)
</dt> </dl>

 

 




