# react-stack-template

import React, { Component } from 'react';
import logo from './logo.svg';
import './App.css';
import UIkit from 'uikit'

import dark from './dark.jpg'
import light from './light.jpg'

import Card from './Components/Card';
import MediaCard from './Components/MediaCard';
import BadgeCard from './Components/BadgeCard';

class App extends Component {

    componentDidMount(){
        var stickys = UIkit.sticky('#sticky', {
            offset: 50
        });
    }

    render() {
        return (
            <div>
                {/*
                <div data-uk-sticky="offset: 50;">
                    test 
                </div>
                */}

                <div className="uk-cover-container uk-height-medium">
                    <img src={dark} alt="" uk-cover />
                    <div>test</div>
                    
                </div>
                
                <br/>

                <div className="content uk-margin-small-left uk-margin-small-right">
                    <div className="uk-column-1-3@l" uk-grid>
                        <div> 
                            <Card/>
                        </div>
                        <div>
                            <Card/>
                        </div>
                        <div>
                            <Card/>
                        </div>
                    </div>

                    <br/><br/>

                    <div className="uk-column-1-2@l" uk-grid>
                        <div>
                            <MediaCard/>
                        </div>
                        <div>
                            <MediaCard/>
                        </div>
                    </div>
                    
                    <div className="uk-column-1-3@l uk-child-width-1-3@l" uk-grid>
                        <BadgeCard/>
                    </div>

                    <div className="uk-child-width-1-3@l" uk-grid>
                        <BadgeCard/>
                        <BadgeCard/>
                    </div>

                    <div className="uk-child-width-1-3@l" uk-grid>
                        <BadgeCard/>
                        <BadgeCard/>
                        <BadgeCard/>
                    </div>

                    <hr/>

                    <div className="uk-child-width-1-3@l" uk-grid uk-scrollspy="cls: uk-animation-fade; target: .uk-card; delay: 500; repeat: false">
                        <BadgeCard/>
                        <BadgeCard/>
                        <BadgeCard/>
                        <BadgeCard/>
                        <BadgeCard/>
                    </div>
                    
                </div>
                
            </div>
        );
    }
}

export default App;
