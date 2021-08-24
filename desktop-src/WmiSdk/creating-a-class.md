---
description: 在 WMI 中，類別是一種物件，可描述企業的某些層面，例如特殊類型的磁片磁碟機。
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: 建立 WMI 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2db62f1f0d14035f7bcc3fd74f8bbbfbacf08cb0dbf139b06c9870b7039e19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612558"
---
# <a name="creating-a-wmi-class"></a>建立 WMI 類別

在 WMI 中，類別是一種物件，可描述企業的某些層面，例如特殊類型的磁片磁碟機。 建立類別定義之後，請撰寫您的提供者 DLL，以提供類別的實例、屬性資料，以及針對該類別定義的執行方法。 然後，腳本和應用程式可以取得資料或控制裝置。 如需詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。

> [!Note]  
> 若要確保如果 WMI 發生失敗並重新啟動，managed 物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請在您的 MOF 檔案中使用 [**\# pragma 自動**](pragma-autorecover.md)復原語句預處理器指令。

 

## <a name="base-class"></a>基類

基類代表一些一般概念。 例如， [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) 類別代表 WMI 中所有類型的 cd-rom 光碟機，並且包含描述所有 cd-rom 光碟機種類的一般屬性。 如需詳細資訊，請參閱 [建立基類（Base Class](creating-a-base-class.md)）。

衍生的類別會繼承其他類別的屬性和方法。 衍生類別通常代表基類的特定案例。 例如， [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive)類別代表 Windows 系統上的 cd-rom 光碟機。 **Win32 \_ CDROMDrive** 類別是以和繼承 [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive)的許多屬性為基礎。 不過， **Win32 \_ CDROMDrive** 和其他衍生類別一樣，可以有讓衍生類別成為唯一的其他屬性。 如需詳細資訊，請參閱 [建立衍生類別](creating-a-derived-class.md)。

## <a name="properties-and-methods"></a>屬性和方法

建立類別表示定義描述該類別的屬性。 您也可以定義方法，以操作類別所代表的物件。

一般來說，屬性代表物件的某個層面，例如裝置的序號或進程的位元組大小，而方法則代表會變更裝置或邏輯實體之狀態或行為的動作。

每個類別都至少必須有一個索引鍵屬性。 雖然類別可以有多個索引鍵，但您無法使用256個以上的索引鍵來建立類別的實例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
