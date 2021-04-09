---
description: Windows Server 2008 R2 將伺服器端手寫辨識的支援新增至 Windows。 本主題說明如何在 Windows Server 2008 R2 中辨識手寫。
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Windows Server 2008 R2 中的手寫辨識
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024291"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a>Windows Server 2008 R2 中的手寫辨識

Windows Server 2008 R2 支援伺服器端的手寫辨識。 伺服器端辨識可讓伺服器辨識網頁上手寫筆輸入的內容。 當網路上的使用者將會指定使用自訂字典來解讀的字詞時，這特別有用。 例如，如果您的醫療應用程式會查詢伺服器資料庫中的患者名稱，這些名稱可能會新增至從手寫 Silverlight 表單執行搜尋時，會交叉參考的另一個資料庫。

## <a name="set-up-your-server-for-server-side-recognition"></a>設定您的伺服器進行 Server-Side 辨識

您應遵循下列步驟來設定伺服器端識別。

- 安裝筆跡和手寫服務
-  (IIS) 和應用程式伺服器安裝 Web 服務器的支援
- 啟用桌面體驗角色
- 啟動 Tablet PC 輸入服務

### <a name="install-ink-and-handwriting-services"></a>安裝筆跡和手寫服務

若要安裝筆跡和手寫服務，請按一下快速啟動紙匣中的 [伺服器管理員] 圖示，以開啟 [伺服器管理員]。 在 [ **功能** ] 功能表中，按一下 [ **新增功能**]。 請確定選取 [ **筆跡和手寫服務** ] 核取方塊。 下圖顯示已選取 **筆跡和手寫服務** 的 [**選取功能**] 對話方塊。

![選取 [筆跡和手寫服務] 核取方塊的 [選取功能] 對話方塊](images/setup-server-1-ink-and-handwriting.png)<br/>
*選取 [筆跡和手寫服務] 核取方塊的 [選取功能] 對話方塊*

### <a name="installation-support-for-web-server-iis-and-application-server"></a>Web 服務器 (IIS) 和應用程式伺服器的安裝支援

開啟 [伺服器管理員]，如同您在第一個步驟中所做的一樣。 接下來，您必須將 Web 服務器 (IIS) 和應用程式伺服器角色。 在 [ **角色** ] 功能表中，按一下 [ **新增角色**]。 [新增角色] wizard 隨即出現。 按一下 [下一步] 。 確定已選取 [ **應用程式伺服器** ] 和 [ **WEB 伺服器 (IIS)** 。 下圖顯示 [ **選取伺服器角色** ] 對話方塊，其中已選取 **網頁伺服器 (IIS)** 和 **應用程式伺服器** 角色。

![選取 [伺服器角色] 對話方塊，其中已選取 web 伺服器 (iis) 和應用程式伺服器角色](images/setup-server-2-select-server-roles.png)<br/>
*選取 [伺服器角色] 對話方塊，其中已選取 web 伺服器 (iis) 和應用程式伺服器角色*

當您選取 [ **應用程式伺服器**] 時，系統會要求您安裝 ASP.NET framework。 按一下 [ **新增所需的功能** ] 按鈕。 按一下 **[下一步**] 之後，您會看到 [總覽] 對話方塊;按 **[下一步]**。 [ **選取角色服務** ] 對話方塊現在應該可以使用。 確定已選取 [ **網頁伺服器 (IIS)** 。 下圖顯示 [ **選取角色服務** ] 對話方塊，其中已啟用 Web 服務器 (IIS) 。

![啟用 web 伺服器 (iis) 的 [選取角色服務] 對話方塊](images/setup-server-3-select-role-services.png)<br/>
*啟用 web 伺服器 (iis) 的 [選取角色服務] 對話方塊*

按一下 [下一步] 。 [總覽] 對話方塊隨即出現;再次按 **[下一步]** 。 您現在會看到一個頁面，提供您選項給 Web 服務器 (IIS) 的角色。 按一下 [下一步] 。 在下一個頁面上，[ **安裝** ] 按鈕將會變成作用中狀態。 按一下 [ **安裝** ]，您將會安裝 Web 服務器 (IIS) 和應用程式伺服器的支援。

### <a name="enable-the-desktop-experience-role"></a>啟用桌面體驗角色

若要啟用 [桌面體驗]，請按一下 [ **開始**]，按一下 [系統 **管理工具**]，然後按一下 [ **伺服器管理員**]。 選取 [ **新增服務** ]，然後選取 [ **桌面體驗** ] 服務。 下圖顯示已安裝桌面體驗專案的 [ **選取功能** ] 對話方塊。

![選取 [桌面體驗服務] 的 [選取功能] 對話方塊](images/setup-server-4-desktop-experience.png)<br/>
*選取 [桌面體驗服務] 的 [選取功能] 對話方塊*

按 **[下一步]** 安裝桌面體驗。

### <a name="start-the-tablet-service"></a>啟動平板電腦服務

安裝桌面體驗服務之後，Tablet PC 輸入服務將會出現在 [ **服務** ] 功能表中。 若要存取 [ **服務** ] 功能表，請按一下 [ **開始**]，按一下 [系統 **管理工具**]，然後按一下 [ **服務**]。 若要啟動服務，請在 [ **TABLET PC 輸入服務** ] 上按一下滑鼠右鍵，然後按一下 [ **啟動**]。 下圖顯示 Tablet PC 輸入服務啟動的 [ **服務** ] 功能表。

![已啟動 tablet pc 輸入服務的 [服務] 功能表](images/setup-server-5-tablet-pc-input-service.png)<br/>
*已啟動 tablet pc 輸入服務的 [服務] 功能表*

## <a name="performing-server-side-recognition-using-silverlight"></a>使用 Silverlight 執行 Server-Side 辨識

本節說明如何建立使用 Silverlight 來捕捉手寫輸入的 Web 應用程式。 使用下列步驟，在 Visual Studio 2008 中編寫辨識器的程式。

- 安裝和更新 Visual Studio 2008 以新增 Silverlight 的支援。
- 在 Visual Studio 2008 中建立新的 Silverlight 專案。
- 將必要的服務參考新增至您的專案。
- 建立手寫辨識的 Silverlight WCF 服務。
- 將服務參考加入至您的用戶端專案。
- 將 InkCollector 類別新增至 InkRecognition 專案。
- 從用戶端設定移除安全傳輸指示詞

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a>安裝和更新 Visual Studio 2008 以新增 Silverlight 支援

開始之前，您必須在 Windows Server 2008 R2 伺服器上執行下列步驟。

- 安裝 Visual Studio 2008。
- 安裝 [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986)。
- 安裝 [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/)。

安裝這些應用程式和更新之後，您就可以開始建立您的伺服器端識別 Web 應用程式。

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a>在 Visual Studio 2008 中建立新的 Silverlight Web 專案

從 [檔案] 功能表，按一下 [新增專案]。 從 Visual C 專案清單中選取 [Silverlight 應用程式] 範本 \# 。 命名您的專案 InkRecognition，然後按一下 **[確定]**。 下圖顯示 \# 已選取的 C Silverlight 專案並命名為 InkRecognition。

![已 \# 選取 c silverlight 專案，名稱為 inkrecognition](images/project-1-new-project.png)<br/>
*已 \# 選取 c silverlight 專案，名稱為 inkrecognition*

按一下 **[確定**] 之後，會出現一個對話方塊，提示您將 Silverlight 應用程式新增至您的專案。 選取 **[將新的 ASP.NET Web 專案加入至方案來裝載 Silverlight** ]，然後按一下 **[確定]**。 下圖顯示如何設定範例專案，然後再按一下 **[確定]**。

![提示將 silverlight 應用程式新增至專案的對話方塊](images/project-2-add-a-new-aspnetproject.png)<br/>
*提示將 silverlight 應用程式新增至專案的對話方塊*

### <a name="add-the-necessary-service-references-to-your-project"></a>將必要的服務參考新增至您的專案

現在您已將一般 Silverlight 用戶端專案 (InkRecognition) 與 Web 專案搭配使用， () InkRecognition 在您的方案中設定。 專案將會開啟，並開啟頁面。 xaml 和 default.aspx。 關閉這些視窗，並以滑鼠右鍵按一下 InkRecognition 專案中的 [參考] 資料夾，然後選取 [ **加入參考**]，將 System.string 和 system.servicemodel 參考新增至 InkRecognition 專案。 下圖顯示已選取必要參考的對話方塊。

![[加入參考] 對話方塊，其中已選取 [system.object] 和 [system.servicemodel]](images/project-3a-add-references-to-inkreco.png)<br/>
*[加入參考] 對話方塊，其中已選取 [system.object] 和 [system.servicemodel]*

接下來，您必須將 System.servicemodel 和 InkRecognition 的參考加入至 Web 專案。 根據預設，Microsoft Ink 參考不會出現在 .NET 參考中，因此請在您的 Windows 資料夾中搜尋 Microsoft.Ink.dll。 在您找到 DLL 之後，請將元件新增至專案參考：選取 [ **流覽** ] 索引標籤，變更至包含 Microsoft.Ink.dll 的資料夾，選取 [Microsoft.Ink.dll]，然後按一下 **[確定]**。 下圖顯示 Windows 檔案總管中的專案方案，並加入所有參考元件。

![已新增所有參考元件的 windows explorer 中的 inkrecognition 專案](images/project-3b-with-reference-assemblies.png)<br/>
*已新增所有參考元件的 windows explorer 中的 inkrecognition 專案*

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a>建立手寫辨識的 Silverlight WCF 服務

接下來，您會將筆跡辨識的 WCF 服務新增至專案。 以滑鼠右鍵按一下 [InkRecognition] 專案，按一下 [ **加入**]，然後按一下 [ **新增專案**]。 選取 [WCF Silverlight 服務] 範本，將名稱變更為 InkRecogitionService，然後按一下 [ **新增**]。 下圖顯示 [ **加入新專案** ] 對話方塊，其中已選取並命名 Silverlight WCF 服務。

![[新增專案] 對話方塊，其中已選取並命名 silverlight wcf 服務](images/project-4-add-wcf-service.png)<br/>
*[新增專案] 對話方塊，其中已選取並命名 silverlight wcf 服務*

新增 WCF Silverlight 服務之後，將會開啟服務程式代碼後 InkRecognitionService。 以下列程式碼取代服務程式代碼。

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a>將服務參考加入至您的用戶端專案

現在您已擁有適用于 InkRecognition 的 Silverlight WCF 服務，您將會從用戶端應用程式取用服務。 以滑鼠右鍵按一下 [InkRecognition] 專案，然後選取 [ **加入服務參考**]。 從顯示的 [ **加入服務參考** ] 對話方塊中，選取 [ **探索** ] 以從目前的方案探索服務。 InkRecognitionService 將會出現在 [服務] 窗格中。 按兩下 [服務] 窗格中的 [InkRecognitionService]，將命名空間變更為 InkRecognitionServiceReference，然後按一下 **[確定]**。 下圖顯示已選取 InkRecognitionService 並變更命名空間的 [ **加入服務參考** ] 對話方塊。

![已選取 inkrecognitionservice 並變更命名空間的 [加入服務參考] 對話方塊](images/project-5-discover-service-reference.png)<br/>
*已選取 inkrecognitionservice 並變更命名空間的 [加入服務參考] 對話方塊*

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a>將 InkCollector 類別新增至 InkRecognition 專案

以滑鼠右鍵按一下 [InkRecognition] 專案，按一下 [ **加入**]，然後按一下 [ **新增專案**]。 從 **Visual C \#** 功能表選取 **C \# 類別**。 將類別命名為 InkCollector。 下圖顯示 \# 已選取 C 類別並命名的對話方塊。

![[加入新專案] 對話方塊 \# ，其中已選取 c 類別並命名為](images/project-6-add-ink-collector.png)<br/>
*[加入新專案] 對話方塊 \# ，其中已選取 c 類別並命名為*

加入 InkCollector 類別之後，將會開啟類別定義。 將筆墨收集器中的程式碼取代為下列程式碼。

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a>更新預設頁面的 XAML，並加入手寫辨識的程式碼後置於

現在您已有一個可收集筆跡的類別，您必須使用下列 XAML 更新頁面中的 XAML。 下列程式碼會將黃色漸層新增至輸入區域、InkCanvas 控制項，以及將觸發辨識的按鈕。

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

以下列程式碼取代 [程式碼後頁] 頁面，將會加入 [ **辨識** ] 按鈕的事件處理常式。

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a>從用戶端設定移除安全傳輸指示詞

在您可以取用 WCF 服務之前，您必須從服務設定移除所有安全傳輸選項，因為 Silverlight 2.0 WCF 服務目前不支援安全傳輸。 從 InkRecognition 專案中，更新 ServiceReferences. ClientConfig 中的安全性設定。 變更安全性 XML 來源

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

to

```XML
       <security mode="None"/>
```

現在，您的應用程式應該會執行。 下圖顯示應用程式在 awebpagewith 中輸入的一些手寫內容。

![Awebpagewith 中的應用程式在辨識方塊中輸入的一些手寫](images/demo-1.png)<br/>
*Awebpagewith 中的應用程式在辨識方塊中輸入的一些手寫*

下圖顯示 [ **結果** ] 下拉式清單中的已辨識文字。

![Awebpagewith 中的應用程式已辨識結果下拉式清單中的文字](images/demo-2.png)<br/>
*Awebpagewith 中的應用程式已辨識結果下拉式清單中的文字*

 

 



