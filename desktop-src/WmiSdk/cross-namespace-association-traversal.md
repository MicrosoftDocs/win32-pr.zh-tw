---
description: 從 Windows 7 開始，Windows Management Instrumentation (WMI) 使用 CIM 架構來實行探索設定檔的標準機制。
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: 跨命名空間關聯的遍歷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848746"
---
# <a name="cross-namespace-association-traversal"></a>跨命名空間關聯的遍歷

從 Windows 7 開始，Windows Management Instrumentation (WMI) 使用 CIM 架構來實行探索設定檔的標準機制。

WMI 支援跨命名空間關聯的遍歷和關聯設定檔註冊。 如需設定檔註冊和關聯性的 CIM 標準執行的詳細資訊，請參閱 DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf)) 

為了支援這項功能，WMI 基礎結構會執行下列動作：

-   建立 interop 命名空間： \\ 根 \\ interop。
-   允許的跨命名空間關聯遍歷。 跨命名空間的關聯支援在關聯類別層級和實命名空間層級進行篩選。
-   已新增 [**cim \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))、 [**cim \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)和 [**cim \_ ReferencedProfile**](cim-referencedprofile.md) 類別。
-   實作為2.17.1 相容性的 CIM 架構版本。 如需詳細資訊，請參閱 [CIM 架構相容性](cim-schema-compatibility.md)。

## <a name="interop-namespace"></a>Interop 命名空間

Interop 命名空間提供一個共同的位置，讓用戶端應用程式探索電腦支援的所有設定檔。 設定檔可用於管理作業系統、存放裝置陣列或資料庫的各種層面。

所有 interop 類別和物件都必須在根 \\ interop 命名空間中定義。

## <a name="cim-classes"></a>CIM 類別

下列清單中所述的 CIM 類別支援跨命名空間關聯的遍歷。

<dl> <dt>

<span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dd>

用來識別公告為已執行的設定檔規格。 這個類別會指定包含設定檔名稱、組織以及符合規範之版本的資訊。

</dd> <dt>

<span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dd>

用來將設定檔中所定義之管理專案的實例與 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) 類別建立關聯，以識別所要執行的特定設定檔規格。

</dd> <dt>

<span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM \_ ReferencedProfile**](cim-referencedprofile.md)
</dt> <dd>

用來表示設定檔之間的關聯性。

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a>執行跨命名空間關聯的遍歷

WMI 服務允許跨命名空間關聯的遍歷。 WMI 提供用來註冊設定檔的 interop 命名空間，並將其與在不同命名空間中執行的設定檔產生關聯。 不過，若要使用關聯性遍歷，實作者必須在 interop 和已執行的命名空間中具現化設定檔類別。 如需詳細資訊，請參閱 [撰寫 Interop 的關聯提供者](writing-an-association-provider-for-interop.md)。

在同一個管理環境內跨命名空間的關聯，必須同時具現化于 interop 和已執行的命名空間中。 否則，關聯遍歷將無法運作。 例如，power profile 關聯提供者必須向根/interop 和根/cimv2/power 命名空間進行註冊。 關聯分析應該能夠從任一命名空間傳回另一個。 如需關聯的範例，請參閱 [存取 Interop 命名空間中的資料](accessing-data-in-the-interop-namespace.md)。

* * Windows Vista： * *

升級到 Windows 7 之後，如果有先前安裝在根/interop 命名空間中的 interop 裝置設定檔，則不會安裝任何 Windows 7 設定檔。 這些協力廠商設定檔物件會覆寫 Windows 7 interop 架構以維護功能。 此外，也會記錄 WMI 應用程式事件識別碼5631。

若要取得 Windows 7 interop 設定檔，必須編譯 Windows 7 版本的 Interop. mof 檔案和相關的 MFL 檔。 如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM \_ ReferencedProfile**](cim-referencedprofile.md)
</dt> <dt>

[CIM 架構相容性](cim-schema-compatibility.md)
</dt> <dt>

[撰寫 Interop 的關聯提供者](writing-an-association-provider-for-interop.md)
</dt> <dt>

[存取 Interop 命名空間中的資料](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
