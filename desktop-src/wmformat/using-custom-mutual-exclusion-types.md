---
title: 使用自訂相互排除類型
description: 使用自訂相互排除類型
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- 相互排除，IWMMutualExclusion 介面
- 相互排除，自訂類型
- 設定檔，自訂相互排除類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092542"
---
# <a name="using-custom-mutual-exclusion-types"></a>使用自訂相互排除類型

您可以使用設定檔中的相互排除物件來符合自訂案例的需求。 藉由將未知的 GUID 值 CLSID \_ WMMUTEX 傳遞 \_ 至 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)，您會通知互斥物件您正在使用自訂案例。

當您讀取具有自訂互斥值的檔案時，您必須手動控制資料流程選取範圍。 讀取器物件將使用您新增至互斥的第一個資料流程作為預設值。

使用下列步驟來建立自訂的互斥物件，並將其新增至設定檔：

1.  藉由呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數來建立配置檔案管理員。
2.  請從現有的設定檔開始，或建立一個全新的設定檔。
    -   如果您使用現有的設定檔，請呼叫 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面的其中一個 load 方法。 然後跳至步驟4。
    -   如果您要建立全新的設定檔，請呼叫 [**IWMProfileManager：： CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile)。
3.  藉由呼叫 [**IWMProfile：： CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)，將資料流程新增至新的設定檔。 使用 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)的方法視需要設定資料流程。 您也可以呼叫 **QueryInterface** 來存取資料流程設定物件中的其他介面。

    **CreateNewStream** 只會建立資料流程設定物件，且不會影響設定檔。 正確設定資料流程之後，您必須呼叫 [**IWMProfile：： AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) 將資料流程新增至設定檔。

4.  藉由呼叫 [**IWMProfile：： CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion)來建立相互排除物件。
5.  藉由呼叫 [**IWMStreamList：： AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (可直接從 [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)) 繼承的 [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)，將所需的資料流程新增至相互排除物件。
6.  藉由呼叫 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)，將相互排除的型別設定為 custom。 將未知的 CLSID \_ WMMUTEX 傳遞 \_ 為類型 GUID。
7.  藉由呼叫 [**IWMProfile：： AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)，將設定的互斥物件新增至設定檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMMutualExclusion 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMProfile 介面**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**IWMStreamConfig 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**IWMStreamList 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**使用相互排除**](using-mutual-exclusion.md)
</dt> <dt>

[**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




