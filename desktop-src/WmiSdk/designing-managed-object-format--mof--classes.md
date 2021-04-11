---
description: WMI 提供者是由受控物件格式 (MOF) 檔案和 DLL 檔案所組成。 MOF 檔案會定義提供者執行提供資料的類別。
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: 設計受控物件格式 (MOF) 類別
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 201f8c45f7a247fbca5695baa6dd440fc5dc323f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193645"
---
# <a name="designing-managed-object-format-mof-classes"></a>設計受控物件格式 (MOF) 類別

[*WMI 提供者*](gloss-p.md)是由受控物件格式 (MOF) 檔案和 DLL 檔案所組成。 MOF 檔案會定義提供者執行提供資料的類別。

MOF 類別定義是由 [**mofcomp.exe**](mofcomp.md) 公用程式所編譯並儲存在 [*WMI 存放庫*](gloss-w.md)中，也稱為通用訊息模型 (CIM) 存放庫。 建立類別的較常見方式是透過 [適用于 WMI 的 COM API](com-api-for-wmi.md)方法。

> [!Note]  
> 若要確保在 WMI 發生失敗並重新啟動時，managed 物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請在您的 MOF 檔案中使用 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。

 

本主題將討論下列各節：

-   [定義要管理的物件](#defining-the-objects-to-manage)
-   [定義屬性或方法](#defining-properties-or-methods)
-   [彼此相關的物件](#relating-objects-to-each-other)
-   [相關主題](#related-topics)

## <a name="defining-the-objects-to-manage"></a>定義要管理的物件

在您識別要管理的企業部分之後，請定義要管理的物件。 定義必須包含所需的資料，並可讓您精確地執行相關的商務規則。 您可以在更細微的層級定義物件，但最好是決定定義中所包含的詳細資料層級，而且需要提供足夠的詳細資料，才能發揮效用。 程式初期的快捷方式可以節省時間，但未來可能會導致更多工作。

分散式管理工作強制 (DMTF) 網站的 CIM 教學課程包含設計流程的絕佳資訊。 如需詳細資訊，請參閱 [www.dmtf.org](https://www.dmtf.org/)。

當您開發和實行架構設計時，請考慮下列因素：

-   限定詞

    限定詞提供如何描述類別、物件、屬性、方法和參數的相關資訊;而且它們會套用至類別和屬性定義。 在 MOF 程式碼中，限定詞會以括弧括住，而且可能包含 \[ 金鑰 \] 或 \[ 關聯 \] 。 如需詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md) 和 [WMI 限定詞](wmi-qualifiers.md)。

-   命名空間

    命名空間是用來分組類別和物件的邏輯單元，以及控制範圍和可見度。 一般而言，命名空間包含一組類別和物件，代表特定環境中的 managed 物件。 如需詳細資訊，請參閱 [在 WMI 中建立](creating-hierarchies-within-wmi.md)階層。

-   Object

    模型化物件可能是架構的實體或邏輯元素。 例如，您可以建立實體磁片磁碟機（例如硬碟）或邏輯磁片（可以是實體磁片上的磁碟分割）的模型。 使用類別來建立實體磁片磁碟機模型的設計，然後擴充該類別以建立邏輯磁片的模型，會比嘗試為每一種磁片類型建立個別類別的擴充性更容易擴充。

-   資料

    資料可能是動態或靜態的。 如果資料是動態的，您必須為它建立類別提供者。

    若要讓使用者修改資料，您必須使用使用者所呼叫的方法，判斷您是否想要讓屬性只能直接寫入或修改。

## <a name="defining-properties-or-methods"></a>定義屬性或方法

一般而言，WMI 類別屬性類似于 c + + 類別中的屬性。 如果您的程式碼針對資料所實行的唯一動作是取得值或設定值，則應該將資料定義為 WMI 類別的屬性。

WMI 方法通常會執行動作來變更受管理物件的狀態。 例如，如果動作是要啟用或停用硬體物件的操作，則最好是建立讀取/寫入屬性的方法。 您也可以決定建立顯示硬體狀態的屬性。

當您建立類別或實例時，您可以加入批註。 您可以使用這項技術來記錄您的類別，或說明程式設計技巧。 如需詳細資訊，請參閱 [建立批註](creating-a-comment.md)。 此外，您可以加入資料來限定資料物件的用途。 如需詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。

## <a name="relating-objects-to-each-other"></a>彼此相關的物件

有兩種方式可以讓物件彼此產生關聯：藉由建立個別的物件，以及關聯的關聯物件，或在另一個物件中嵌入一個物件。 CIM 不支援内嵌物件，因此若要符合 CIM 規範，您必須使用第一個方法。 不過，WMI 支援內嵌物件，因此請使用這兩種方法來表示物件之間的關聯性。 您可以在 [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider)中找到内嵌物件的範例。 例如， [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 具有内嵌物件 [**Win32 ACE，此 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)具有另一個内嵌物件（ [**win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)）。

在決定如何代表物件之間的關聯性時，請考慮下列事項：

-   如果實例很有用，則關聯最適合。 例如， [**win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 和 [**win32 \_ UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount)。 如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。
-   如果實例不存在父物件的外部，則内嵌物件的效果最佳。 例如， [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 和 [**win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)。 如需詳細資訊，請參閱 [在類別中内嵌物件](embedded-objects.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[將資料提供給 WMI](providing-data-to-wmi.md)
</dt> <dt>

[MOF 資料類型](mof-data-types.md)
</dt> </dl>

 

 
