---
description: COM + 應用程式是由一或多個 COM 元件所組成。
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: COM + 應用程式的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468101"
---
# <a name="parts-of-a-com-application"></a>COM + 應用程式的元件

COM + 應用程式是由一或多個 COM 元件所組成。

COM + 檔中使用下列詞彙：

<dl> <dt>

<span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*COM 元件*
</dt> <dd>

建立 COM 物件 (包含封裝和註冊程式碼) 的二進位單位程式碼。

</dd> <dt>

<span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*COM 物件*
</dt> <dd>

COM 類別的實例。

</dd> <dt>

<span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*COM 類別*
</dt> <dd>

一或多個介面的已命名、具體實作為。 COM 類別是以 CLSID 識別 (有時也會) ProgID。

</dd> <dt>

<span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*COM 介面*
</dt> <dd>

由指定合約的 COM 類別所公開的一組相關的方法函數。 這包括 name、interface signature、interface 語義和封送處理緩衝區格式。 介面是由 IID 識別。 介面語法定義于 IDL 和/或類型程式庫中。 COM 類別的介面應該分割成可管理且一致的方法集合。

COM 介面是不可變的;COM 合約指出無法修改它們。 任何修改 (例如新增方法) 都需要定義新的介面。

</dd> <dt>

<span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*COM 方法*
</dt> <dd>

COM 介面所提供的一組相關函數之一。

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a>已設定和未設定的元件

為了充分利用 COM + 應用程式所支援的服務，COM + 環境會針對 com + 應用程式所建立的 COM 元件強加特定需求。 當將 COM 元件加入至 COM + 應用程式時，就稱為 *已設定的元件*。

針對 COM + 應用程式所建立的 COM 元件是同進程伺服器元件。 元件必須包含類型程式庫 ( .tlb 檔) 來描述在元件中實建的所有類別，並在元件的所有類別上宣告介面。 您可以使用 Microsoft Visual Basic、Microsoft Visual C++ 或任何 COM 相容開發工具來建立及執行這些元件。

未設定的 *元件* 是未安裝在 com + 應用程式中的元件。 您可以藉由將大部分未設定的元件整合至 COM + 應用程式，將這些元件轉換成已設定的元件。

> [!Note]  
> 針對 COM + 應用程式和登錄中未設定的元件，請勿使用相同的 AppID。 啟用未設定的元件時，當啟用時，可能會從登錄中取得 COM 啟用所需資訊的 COM + 應用程式資訊。 如果從裝載 COM + 伺服器應用程式的 Dllhost.exe 呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) ，可能會發生類似的問題。

 

 

 
