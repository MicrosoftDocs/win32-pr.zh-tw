---
title: 設定資料單位延伸模組
description: 設定資料單位延伸模組
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- 資料流程，設定資料單位延伸模組
- 資料流程，資料單位延伸
- 資料單位延伸模組，設定
- 設定檔，資料單位延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "103681544"
---
# <a name="configuring-data-unit-extensions"></a>設定資料單位延伸模組

寫入至 ASF 檔案的範例可包含媒體範例本身以外的其他資訊。 這項資訊包含在使用資料單位延伸模組中。 如需資料單位延伸的詳細資訊，請參閱 [資料單位延伸](data-unit-extensions.md)。

若要使用資料單位延伸模組，您必須設定設定檔中的串流以接受這些延伸模組。 若要設定資料流程的資料單位延伸，請執行下列步驟。

1.  藉由呼叫 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)的 **QueryInterface** 方法，取得 [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)介面的指標。
2.  呼叫 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 來註冊資料流程的資料單位延伸模組類型。

您可以藉由呼叫 [**IWMStreamConfig2：： GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) 來取得已註冊之資料單位延伸模組類型的數目，來檢查目前為數據流註冊的所有資料單位延伸模組類型。 然後，您可以使用 [**IWMStreamConfig2：： GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) 的呼叫，逐一執行所有類型的迴圈。

設定資料流程時，會為數據單位延伸模組指派大小。 許多資料單位延伸系統都使用固定大小的資料， (通常是結構) 。 不過，您也可以藉由將大小設定為0xFFFF，將資料單位延伸模組設定為變數大小。 在編碼時間指派的每個資料單位延伸可以是1個位元組到65534個位元組之間的任何大小。 大小可變大小的資料單位延伸也稱為動態資料單位延伸模組。

使用動態資料單位延伸的優點是您可以視需要附加擴充功能資料。 如果您定義具有設定大小的資料單位延伸，則資料流程的每個範例都必須包含該大小的延伸資料，即使您沒有一些範例的資料。 使用動態資料單位延伸模組時，您可以省略一些範例中的資料單位延伸模組，以節省空間並減少頻寬需求。 但是，如果資料單位延伸是變數大小，讀取物件就無法針對靜態大小驗證接收的延伸資料。 您必須確認您收到的延伸模組資料是有效的，而不是位資料流程的惡意失真。

您必須使用 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法，在範例上設定個別的資料單位延伸。 如需詳細資訊，請參閱 [設定資料單位延伸](setting-data-unit-extensions.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> </dl>

 

 




